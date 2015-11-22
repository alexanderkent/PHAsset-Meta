# PHAsset-Meta
PHAsset category to simplify image meta / exif operations

### Description
```

/*!
 @method        requestUniformTypeWithCompletionBlock
 @description   Get system-declared uniform type identifiers of an asset 
                (com.compuserve.gif, public.png, etc)
 @param         completionBlock This block is passed a string. 
                This parameter may be nil.
 */
-(void)requestUniformTypeWithCompletionBlock:(PHAssetStringBlock)completionBlock;

/*!
 @method        requestMetadataWithOptions:options:completionBlock
 @description   Get metadata dictionary of an asset 
                (contains sub-dictionaries EXIF, GPS etc)
 @param         options to specify options of a PHAsset object 
                (networkAccessAllowed, progressHandler)
 @param         completionBlock This block is passed a dictionary of metadata properties. 
                This parameter may be nil.
 */
-(void)requestMetadataWithOptions:(PHContentEditingInputRequestOptions*)options 
                  completionBlock:(PHAssetMetadataBlock)completionBlock;


/*!
 @method        requestMetadataWithCompletionBlock
 @description   Get metadata dictionary of an asset (contains sub-dictionaries EXIF, GPS etc)
 @param         completionBlock This block is passed a dictionary of metadata properties. This parameter may be nil.
 */
-(void)requestMetadataWithCompletionBlock:(PHAssetMetadataBlock)completionBlock;

```

### Metadata

The requestMetadataWithOptions method returns a meta-dictionary with sub-dictionaries per Apple's ImageIO framework.

```
{
    ColorModel = RGB;
    DPIHeight = 72;
    DPIWidth = 72;
    Depth = 8;
    Orientation = 1;
    PixelHeight = 2848;
    PixelWidth = 4288;
    ProfileName = "Adobe RGB (1998)";
    "{Exif}" =     {
        ColorSpace = 1;
        ComponentsConfiguration =         (
            1,
            2,
            3,
            0
        );
        DateTimeDigitized = "2011:03:12 16:17:25";
        DateTimeOriginal = "2011:03:12 16:17:25";
        ExifVersion =         (
            2,
            2
        );
        ExposureBiasValue = 0;
        ExposureProgram = 3;
        ExposureTime = "0.000625";
        FNumber = 4;
        Flash = 0;
        FlashPixVersion =         (
            1,
            0
        );
        FocalLength = 26;
        ISOSpeedRatings =         (
            200
        );
        LightSource = 14;
        MaxApertureValue = 4;
        MeteringMode = 5;
        PixelXDimension = 4288;
        PixelYDimension = 2848;
        SceneCaptureType = 0;
        SensingMethod = 2;
    };
    "{GPS}" =     {
        Latitude = "38.0374445";
        LatitudeRef = N;
        Longitude = "122.8031783333333";
        LongitudeRef = W;
    };
    "{IPTC}" =     {
        DateCreated = 20110312;
        DigitalCreationDate = 20110312;
        DigitalCreationTime = 161725;
        ObjectName = "DSC_0001";
        TimeCreated = 161725;
    };
    "{JFIF}" =     {
        DensityUnit = 1;
        JFIFVersion =         (
            1,
            0,
            1
        );
        XDensity = 72;
        YDensity = 72;
    };
    "{TIFF}" =     {
        DateTime = "2011:05:03 20:30:44";
        Make = "NIKON CORPORATION";
        Model = "NIKON D90";
        Orientation = 1;
        PhotometricInterpretation = 2;
        ResolutionUnit = 2;
        Software = "QuickTime 7.7.1";
        XResolution = 72;
        YResolution = 72;
    };
}
```
