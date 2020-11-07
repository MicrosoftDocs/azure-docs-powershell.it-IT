---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: c76ccab31b3c5c11216a1a929e2a78df55713325
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675327"
---
# <span data-ttu-id="56092-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="56092-101">New-AzImageConfig</span></span>

## <span data-ttu-id="56092-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56092-102">SYNOPSIS</span></span>
<span data-ttu-id="56092-103">Crea un oggetto Image configurabile.</span><span class="sxs-lookup"><span data-stu-id="56092-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="56092-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56092-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56092-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56092-105">DESCRIPTION</span></span>
<span data-ttu-id="56092-106">Il cmdlet **New-AzImageConfig** crea un oggetto Image configurabile.</span><span class="sxs-lookup"><span data-stu-id="56092-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="56092-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56092-107">EXAMPLES</span></span>

### <span data-ttu-id="56092-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56092-108">Example 1</span></span>
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

<span data-ttu-id="56092-109">Il primo comando crea un oggetto Image e lo archivia nella variabile $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="56092-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="56092-110">I tre comandi seguenti assegnano percorsi del disco del sistema operativo e due dischi di dati alle variabili $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="56092-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="56092-111">Questo approccio è solo per la leggibilità dei comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="56092-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="56092-112">I tre comandi seguenti aggiungono un disco del sistema operativo e due dischi di dati all'immagine archiviata in $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="56092-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="56092-113">L'URI di ogni disco è archiviato in $osDiskVhdUri, $dataDiskVhdUri 1 e $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="56092-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="56092-114">Il comando finale crea un'immagine denominata "ImageName01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="56092-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="56092-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56092-115">PARAMETERS</span></span>

### <span data-ttu-id="56092-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="56092-116">-DataDisk</span></span>
<span data-ttu-id="56092-117">Specifica l'oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="56092-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="56092-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56092-118">-DefaultProfile</span></span>
<span data-ttu-id="56092-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56092-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56092-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="56092-120">-HyperVGeneration</span></span>
<span data-ttu-id="56092-121">Specifica il tipo di HyperVGeneration per la macchina virtuale creata dall'immagine.</span><span class="sxs-lookup"><span data-stu-id="56092-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="56092-122">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="56092-122">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56092-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="56092-123">-Location</span></span>
<span data-ttu-id="56092-124">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="56092-124">Specifies a location.</span></span>

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

### <span data-ttu-id="56092-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="56092-125">-OsDisk</span></span>
<span data-ttu-id="56092-126">Specifica il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="56092-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="56092-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="56092-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="56092-128">Specifica l'ID della macchina virtuale di origine.</span><span class="sxs-lookup"><span data-stu-id="56092-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="56092-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="56092-129">-Tag</span></span>
<span data-ttu-id="56092-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="56092-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="56092-131">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="56092-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="56092-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="56092-132">-ZoneResilient</span></span>
<span data-ttu-id="56092-133">Abilita area resiliente</span><span class="sxs-lookup"><span data-stu-id="56092-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="56092-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56092-134">-Confirm</span></span>
<span data-ttu-id="56092-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56092-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56092-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56092-136">-WhatIf</span></span>
<span data-ttu-id="56092-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56092-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56092-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56092-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56092-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56092-139">CommonParameters</span></span>
<span data-ttu-id="56092-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56092-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56092-141">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56092-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56092-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56092-142">INPUTS</span></span>

### <span data-ttu-id="56092-143">System. String</span><span class="sxs-lookup"><span data-stu-id="56092-143">System.String</span></span>

### <span data-ttu-id="56092-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="56092-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="56092-145">Microsoft. Azure. Management. Compute. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="56092-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="56092-146">Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="56092-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="56092-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56092-147">OUTPUTS</span></span>

### <span data-ttu-id="56092-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="56092-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="56092-149">Note</span><span class="sxs-lookup"><span data-stu-id="56092-149">NOTES</span></span>

## <span data-ttu-id="56092-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56092-150">RELATED LINKS</span></span>