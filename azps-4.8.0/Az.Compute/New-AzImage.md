---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: ff291afae70636863dff8ce34b5610cd77ce1251
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032581"
---
# <span data-ttu-id="e8d14-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="e8d14-101">New-AzImage</span></span>

## <span data-ttu-id="e8d14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8d14-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d14-103">Crea un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e8d14-103">Creates an image.</span></span>

## <span data-ttu-id="e8d14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8d14-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8d14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8d14-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d14-106">Il cmdlet **New-azime** crea un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e8d14-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="e8d14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8d14-107">EXAMPLES</span></span>

### <span data-ttu-id="e8d14-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8d14-108">Example 1</span></span>
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

<span data-ttu-id="e8d14-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e8d14-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="e8d14-110">I tre comandi seguenti assegnano percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e8d14-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="e8d14-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8d14-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="e8d14-112">I tre comandi seguenti aggiungono un disco del sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e8d14-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="e8d14-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e8d14-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="e8d14-114">Il comando finale crea un'immagine denominata "ImageName01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e8d14-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e8d14-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8d14-115">PARAMETERS</span></span>

### <span data-ttu-id="e8d14-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8d14-116">-AsJob</span></span>
<span data-ttu-id="e8d14-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e8d14-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8d14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d14-118">-DefaultProfile</span></span>
<span data-ttu-id="e8d14-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d14-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8d14-120">-Immagine</span><span class="sxs-lookup"><span data-stu-id="e8d14-120">-Image</span></span>
<span data-ttu-id="e8d14-121">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="e8d14-121">Specifies a local image object.</span></span>

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

### <span data-ttu-id="e8d14-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e8d14-122">-ImageName</span></span>
<span data-ttu-id="e8d14-123">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e8d14-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="e8d14-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d14-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8d14-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e8d14-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e8d14-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8d14-126">-Confirm</span></span>
<span data-ttu-id="e8d14-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8d14-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8d14-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8d14-128">-WhatIf</span></span>
<span data-ttu-id="e8d14-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8d14-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8d14-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8d14-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8d14-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d14-131">CommonParameters</span></span>
<span data-ttu-id="e8d14-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d14-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d14-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8d14-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d14-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8d14-134">INPUTS</span></span>

### <span data-ttu-id="e8d14-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e8d14-135">System.String</span></span>

### <span data-ttu-id="e8d14-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e8d14-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e8d14-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8d14-137">OUTPUTS</span></span>

### <span data-ttu-id="e8d14-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e8d14-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e8d14-139">Note</span><span class="sxs-lookup"><span data-stu-id="e8d14-139">NOTES</span></span>

## <span data-ttu-id="e8d14-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8d14-140">RELATED LINKS</span></span>
