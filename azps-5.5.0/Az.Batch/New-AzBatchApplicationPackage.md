---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197070"
---
# <span data-ttu-id="e02cd-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e02cd-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="e02cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e02cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e02cd-103">Crea un pacchetto dell'applicazione in un account batch.</span><span class="sxs-lookup"><span data-stu-id="e02cd-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="e02cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e02cd-104">SYNTAX</span></span>

### <span data-ttu-id="e02cd-105">UploadAndActivate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e02cd-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02cd-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="e02cd-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e02cd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e02cd-107">DESCRIPTION</span></span>
<span data-ttu-id="e02cd-108">Il cmdlet **New-AzBatchApplicationPackage** crea un pacchetto dell'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="e02cd-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="e02cd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e02cd-109">EXAMPLES</span></span>

### <span data-ttu-id="e02cd-110">Esempio 1: Installare un pacchetto dell'applicazione in un account batch</span><span class="sxs-lookup"><span data-stu-id="e02cd-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="e02cd-111">Questo comando crea e attiva la versione 1.0 dell'applicazione Litware e carica il contenuto di litware.1.0.zip come contenuto del pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e02cd-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="e02cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e02cd-112">PARAMETERS</span></span>

### <span data-ttu-id="e02cd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e02cd-113">-AccountName</span></span>
<span data-ttu-id="e02cd-114">Specifica il nome dell'account batch a cui questo cmdlet aggiunge un pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e02cd-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="e02cd-115">-ActivateOnly</span></span>
<span data-ttu-id="e02cd-116">Indica che questo cmdlet attiva un pacchetto dell'applicazione già caricato.</span><span class="sxs-lookup"><span data-stu-id="e02cd-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e02cd-117">-ApplicationName</span></span>
<span data-ttu-id="e02cd-118">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e02cd-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="e02cd-119">-ApplicationVersion</span></span>
<span data-ttu-id="e02cd-120">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e02cd-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02cd-121">-DefaultProfile</span></span>
<span data-ttu-id="e02cd-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e02cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e02cd-123">-FilePath</span></span>
<span data-ttu-id="e02cd-124">Specifica il file da caricare come file binario del pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e02cd-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-125">-Format</span><span class="sxs-lookup"><span data-stu-id="e02cd-125">-Format</span></span>
<span data-ttu-id="e02cd-126">Specifica il formato del file binario del pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e02cd-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="e02cd-128">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="e02cd-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02cd-129">CommonParameters</span></span>
<span data-ttu-id="e02cd-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02cd-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e02cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02cd-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e02cd-132">INPUTS</span></span>

### <span data-ttu-id="e02cd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e02cd-133">System.String</span></span>

### <span data-ttu-id="e02cd-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e02cd-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e02cd-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e02cd-135">OUTPUTS</span></span>

### <span data-ttu-id="e02cd-136">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e02cd-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="e02cd-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e02cd-137">NOTES</span></span>

## <span data-ttu-id="e02cd-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e02cd-138">RELATED LINKS</span></span>

[<span data-ttu-id="e02cd-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e02cd-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="e02cd-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e02cd-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="e02cd-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e02cd-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="e02cd-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e02cd-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="e02cd-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e02cd-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="e02cd-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e02cd-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


