---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 25bf6699887219cb4315465d7e0f709f82849438
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863450"
---
# <span data-ttu-id="e182b-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="e182b-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="e182b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e182b-102">SYNOPSIS</span></span>
<span data-ttu-id="e182b-103">Imposta le proprietà di riferimento dell'immagine in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="e182b-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="e182b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e182b-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e182b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e182b-105">DESCRIPTION</span></span>
<span data-ttu-id="e182b-106">Il cmdlet **set-AzDiskImageReference** imposta le proprietà di riferimento dell'immagine su un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="e182b-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="e182b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e182b-107">EXAMPLES</span></span>

### <span data-ttu-id="e182b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e182b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e182b-109">Il primo comando crea un oggetto disco locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e182b-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e182b-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="e182b-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="e182b-111">Il secondo comando imposta l'ID immagine e l'unità logica numero 0 per il disco Obejct.</span><span class="sxs-lookup"><span data-stu-id="e182b-111">The second command sets the image id and the logical unit number 0 for the disk obejct.</span></span>
<span data-ttu-id="e182b-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e182b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e182b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e182b-113">PARAMETERS</span></span>

### <span data-ttu-id="e182b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e182b-114">-DefaultProfile</span></span>
<span data-ttu-id="e182b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e182b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e182b-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="e182b-116">-Disk</span></span>
<span data-ttu-id="e182b-117">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="e182b-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e182b-118">-ID</span><span class="sxs-lookup"><span data-stu-id="e182b-118">-Id</span></span>
<span data-ttu-id="e182b-119">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="e182b-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e182b-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="e182b-120">-Lun</span></span>
<span data-ttu-id="e182b-121">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="e182b-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e182b-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e182b-122">-Confirm</span></span>
<span data-ttu-id="e182b-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e182b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e182b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e182b-124">-WhatIf</span></span>
<span data-ttu-id="e182b-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e182b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e182b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e182b-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e182b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e182b-127">CommonParameters</span></span>
<span data-ttu-id="e182b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e182b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e182b-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e182b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e182b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e182b-130">INPUTS</span></span>

### <span data-ttu-id="e182b-131">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="e182b-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="e182b-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e182b-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e182b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e182b-133">OUTPUTS</span></span>

### <span data-ttu-id="e182b-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="e182b-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="e182b-135">Note</span><span class="sxs-lookup"><span data-stu-id="e182b-135">NOTES</span></span>

## <span data-ttu-id="e182b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e182b-136">RELATED LINKS</span></span>

