---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: 262184f82aa169b5e76d3b875d0e3ba27db4da38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508331"
---
# <span data-ttu-id="d8f45-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="d8f45-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="d8f45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8f45-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f45-103">Imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="d8f45-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8f45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8f45-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <Snapshot> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8f45-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8f45-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f45-106">Il cmdlet **set-AzureRmSnapshotImageReference** imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="d8f45-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="d8f45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8f45-107">EXAMPLES</span></span>

### <span data-ttu-id="d8f45-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8f45-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="d8f45-109">Il primo comando crea un oggetto snapshot locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d8f45-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d8f45-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d8f45-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="d8f45-111">Il secondo comando imposta l'ID immagine e il numero di unità logica 0 per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="d8f45-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="d8f45-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d8f45-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d8f45-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8f45-113">PARAMETERS</span></span>

### <span data-ttu-id="d8f45-114">-ID</span><span class="sxs-lookup"><span data-stu-id="d8f45-114">-Id</span></span>
<span data-ttu-id="d8f45-115">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="d8f45-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="d8f45-116">-Lun</span><span class="sxs-lookup"><span data-stu-id="d8f45-116">-Lun</span></span>
<span data-ttu-id="d8f45-117">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="d8f45-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="d8f45-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="d8f45-118">-Snapshot</span></span>
<span data-ttu-id="d8f45-119">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="d8f45-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f45-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8f45-120">-Confirm</span></span>
<span data-ttu-id="d8f45-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f45-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f45-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f45-122">-WhatIf</span></span>
<span data-ttu-id="d8f45-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8f45-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8f45-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8f45-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f45-125">CommonParameters</span></span>
<span data-ttu-id="d8f45-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f45-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f45-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f45-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8f45-128">INPUTS</span></span>

### <span data-ttu-id="d8f45-129">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="d8f45-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="d8f45-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d8f45-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d8f45-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8f45-131">OUTPUTS</span></span>

### <span data-ttu-id="d8f45-132">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="d8f45-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="d8f45-133">Note</span><span class="sxs-lookup"><span data-stu-id="d8f45-133">NOTES</span></span>

## <span data-ttu-id="d8f45-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8f45-134">RELATED LINKS</span></span>

