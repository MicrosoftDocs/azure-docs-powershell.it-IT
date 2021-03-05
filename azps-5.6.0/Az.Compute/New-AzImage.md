---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: 77a4879d403b52a828460bcfec5666b7071dcea9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959662"
---
# <span data-ttu-id="8c8d9-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="8c8d9-101">New-AzImage</span></span>

## <span data-ttu-id="8c8d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8d9-103">Crea un'immagine.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-103">Creates an image.</span></span>

## <span data-ttu-id="8c8d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c8d9-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c8d9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c8d9-105">DESCRIPTION</span></span>
<span data-ttu-id="8c8d9-106">Il cmdlet **New-AzImage** crea un'immagine.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="8c8d9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c8d9-107">EXAMPLES</span></span>

### <span data-ttu-id="8c8d9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8c8d9-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="8c8d9-109">Il primo comando crea un oggetto immagine e quindi lo archivia nella $imageConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="8c8d9-110">I tre comandi seguenti assegnano i percorsi del disco os e due dischi dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="8c8d9-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="8c8d9-112">I successivi tre comandi aggiungono ciascuno un disco os e due dischi dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="8c8d9-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="8c8d9-114">Il comando finale crea un'immagine denominata 'ImageName01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8c8d9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c8d9-115">PARAMETERS</span></span>

### <span data-ttu-id="8c8d9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c8d9-116">-AsJob</span></span>
<span data-ttu-id="8c8d9-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8c8d9-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8d9-118">-DefaultProfile</span></span>
<span data-ttu-id="8c8d9-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c8d9-120">-Image</span><span class="sxs-lookup"><span data-stu-id="8c8d9-120">-Image</span></span>
<span data-ttu-id="8c8d9-121">Specifica un oggetto immagine locale.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c8d9-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8c8d9-122">-ImageName</span></span>
<span data-ttu-id="8c8d9-123">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c8d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c8d9-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8c8d9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c8d9-126">-Confirm</span></span>
<span data-ttu-id="8c8d9-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8d9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c8d9-128">-WhatIf</span></span>
<span data-ttu-id="8c8d9-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c8d9-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8d9-131">CommonParameters</span></span>
<span data-ttu-id="8c8d9-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8d9-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c8d9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8d9-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c8d9-134">INPUTS</span></span>

### <span data-ttu-id="8c8d9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8c8d9-135">System.String</span></span>

### <span data-ttu-id="8c8d9-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="8c8d9-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="8c8d9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c8d9-137">OUTPUTS</span></span>

### <span data-ttu-id="8c8d9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="8c8d9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="8c8d9-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c8d9-139">NOTES</span></span>

## <span data-ttu-id="8c8d9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c8d9-140">RELATED LINKS</span></span>
