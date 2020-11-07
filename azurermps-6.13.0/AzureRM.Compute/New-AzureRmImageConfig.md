---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: f2d5903de64655b79765774f7232790f8a00ffc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688147"
---
# <span data-ttu-id="59a56-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="59a56-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="59a56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59a56-102">SYNOPSIS</span></span>
<span data-ttu-id="59a56-103">Crea un oggetto Image configurabile.</span><span class="sxs-lookup"><span data-stu-id="59a56-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59a56-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59a56-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59a56-105">DESCRIPTION</span></span>
<span data-ttu-id="59a56-106">Il cmdlet **New-AzureRmImageConfig** crea un oggetto Image configurabile.</span><span class="sxs-lookup"><span data-stu-id="59a56-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="59a56-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59a56-107">EXAMPLES</span></span>

### <span data-ttu-id="59a56-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59a56-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="59a56-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="59a56-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="59a56-110">I tre comandi seguenti assegnano percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="59a56-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="59a56-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="59a56-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="59a56-112">I tre comandi seguenti aggiungono un disco del sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="59a56-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="59a56-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="59a56-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="59a56-114">Il comando finale crea un'immagine denominata "ImageName01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="59a56-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="59a56-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59a56-115">PARAMETERS</span></span>

### <span data-ttu-id="59a56-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="59a56-116">-DataDisk</span></span>
<span data-ttu-id="59a56-117">Specifica l'oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="59a56-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a56-118">-DefaultProfile</span></span>
<span data-ttu-id="59a56-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59a56-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a56-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="59a56-120">-Location</span></span>
<span data-ttu-id="59a56-121">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="59a56-121">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a56-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="59a56-122">-OsDisk</span></span>
<span data-ttu-id="59a56-123">Specifica il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="59a56-123">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a56-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="59a56-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="59a56-125">Specifica l'ID della macchina virtuale di origine.</span><span class="sxs-lookup"><span data-stu-id="59a56-125">Specifies the source virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a56-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="59a56-126">-Tag</span></span>
<span data-ttu-id="59a56-127">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="59a56-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59a56-128">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="59a56-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a56-129">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="59a56-129">-ZoneResilient</span></span>
<span data-ttu-id="59a56-130">Abilita area resiliente</span><span class="sxs-lookup"><span data-stu-id="59a56-130">Enable zone resilient</span></span>

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

### <span data-ttu-id="59a56-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59a56-131">-Confirm</span></span>
<span data-ttu-id="59a56-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59a56-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a56-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a56-133">-WhatIf</span></span>
<span data-ttu-id="59a56-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59a56-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59a56-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59a56-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a56-136">CommonParameters</span></span>
<span data-ttu-id="59a56-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a56-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a56-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a56-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59a56-139">INPUTS</span></span>

### <span data-ttu-id="59a56-140">System. String</span><span class="sxs-lookup"><span data-stu-id="59a56-140">System.String</span></span>

### <span data-ttu-id="59a56-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="59a56-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="59a56-142">Microsoft. Azure. Management. Compute. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="59a56-142">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="59a56-143">Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="59a56-143">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="59a56-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59a56-144">OUTPUTS</span></span>

### <span data-ttu-id="59a56-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="59a56-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="59a56-146">Note</span><span class="sxs-lookup"><span data-stu-id="59a56-146">NOTES</span></span>

## <span data-ttu-id="59a56-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59a56-147">RELATED LINKS</span></span>
