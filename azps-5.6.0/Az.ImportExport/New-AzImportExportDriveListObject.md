---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 4b3907e71dd8d457b1ab38ecd5cdc82b38d7b772
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970829"
---
# <span data-ttu-id="9860c-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="9860c-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="9860c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9860c-102">SYNOPSIS</span></span>
<span data-ttu-id="9860c-103">Creare un oggetto DriverList per ImportExport.</span><span class="sxs-lookup"><span data-stu-id="9860c-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="9860c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9860c-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="9860c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9860c-105">DESCRIPTION</span></span>
<span data-ttu-id="9860c-106">Creare un oggetto DriverList per ImportExport.</span><span class="sxs-lookup"><span data-stu-id="9860c-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="9860c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9860c-107">EXAMPLES</span></span>

### <span data-ttu-id="9860c-108">Esempio 1: Creare un nuovo elenco unità per il processo ImportExport</span><span class="sxs-lookup"><span data-stu-id="9860c-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="9860c-109">Questi cmdlet creano un nuovo processo DriveList for ImportExport.</span><span class="sxs-lookup"><span data-stu-id="9860c-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="9860c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9860c-110">PARAMETERS</span></span>

### <span data-ttu-id="9860c-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="9860c-111">-BitLockerKey</span></span>
<span data-ttu-id="9860c-112">Chiave BitLocker usata per crittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-112">The BitLocker key used to encrypt the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="9860c-113">-BytesSucceeded</span></span>
<span data-ttu-id="9860c-114">Byte trasferiti correttamente per l'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="9860c-115">-CopyStatus</span></span>
<span data-ttu-id="9860c-116">Stato dettagliato sul processo di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="9860c-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="9860c-117">Questo campo non viene restituito nella risposta finché l'unità non è in stato di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="9860c-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="9860c-118">-DriveHeaderHash</span></span>
<span data-ttu-id="9860c-119">Valore hash dell'intestazione dell'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-119">The drive header hash value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="9860c-120">-DriveId</span></span>
<span data-ttu-id="9860c-121">Numero di serie dell'hardware dell'unità, senza spazi.</span><span class="sxs-lookup"><span data-stu-id="9860c-121">The drive's hardware serial number, without spaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="9860c-122">-ErrorLogUri</span></span>
<span data-ttu-id="9860c-123">URI che punta al BLOB contenente il log degli errori per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="9860c-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="9860c-124">-ManifestFile</span></span>
<span data-ttu-id="9860c-125">Percorso relativo del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-125">The relative path of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="9860c-126">-ManifestHash</span></span>
<span data-ttu-id="9860c-127">Hash MD5 codificato in Base16 del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="9860c-128">-ManifestUri</span></span>
<span data-ttu-id="9860c-129">URI che punta al BLOB contenente il file manifesto dell'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-129">A URI that points to the blob containing the drive manifest file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="9860c-130">-PercentComplete</span></span>
<span data-ttu-id="9860c-131">Percentuale di completamento per l'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-132">-State</span><span class="sxs-lookup"><span data-stu-id="9860c-132">-State</span></span>
<span data-ttu-id="9860c-133">Stato corrente dell'unità.</span><span class="sxs-lookup"><span data-stu-id="9860c-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="9860c-134">-VerboseLogUri</span></span>
<span data-ttu-id="9860c-135">URI che punta al BLOB contenente il log dettagliato per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="9860c-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9860c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9860c-136">CommonParameters</span></span>
<span data-ttu-id="9860c-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9860c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9860c-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9860c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9860c-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="9860c-139">INPUTS</span></span>

## <span data-ttu-id="9860c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9860c-140">OUTPUTS</span></span>

### <span data-ttu-id="9860c-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="9860c-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="9860c-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="9860c-142">NOTES</span></span>

<span data-ttu-id="9860c-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9860c-143">ALIASES</span></span>

## <span data-ttu-id="9860c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9860c-144">RELATED LINKS</span></span>

