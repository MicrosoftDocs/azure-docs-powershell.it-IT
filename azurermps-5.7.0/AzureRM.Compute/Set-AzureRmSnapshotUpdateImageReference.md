---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509967"
---
# <span data-ttu-id="65e42-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="65e42-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="65e42-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65e42-102">SYNOPSIS</span></span>
<span data-ttu-id="65e42-103">Imposta le proprietà di riferimento dell'immagine in un oggetto Update snapshot.</span><span class="sxs-lookup"><span data-stu-id="65e42-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65e42-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65e42-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65e42-105">DESCRIPTION</span></span>
<span data-ttu-id="65e42-106">Il cmdlet **set-AzureRmSnapshotUpdateImageReference** imposta le proprietà di riferimento dell'immagine in un oggetto Update snapshot.</span><span class="sxs-lookup"><span data-stu-id="65e42-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="65e42-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65e42-107">EXAMPLES</span></span>

### <span data-ttu-id="65e42-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65e42-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="65e42-109">Il primo comando crea un oggetto aggiornamento snapshot locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65e42-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="65e42-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="65e42-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="65e42-111">Il secondo comando imposta l'ID immagine e il numero di unità logica 0 per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="65e42-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="65e42-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="65e42-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="65e42-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65e42-113">PARAMETERS</span></span>

### <span data-ttu-id="65e42-114">-ID</span><span class="sxs-lookup"><span data-stu-id="65e42-114">-Id</span></span>
<span data-ttu-id="65e42-115">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="65e42-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="65e42-116">-Lun</span><span class="sxs-lookup"><span data-stu-id="65e42-116">-Lun</span></span>
<span data-ttu-id="65e42-117">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="65e42-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="65e42-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="65e42-118">-SnapshotUpdate</span></span>
<span data-ttu-id="65e42-119">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="65e42-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65e42-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65e42-120">-Confirm</span></span>
<span data-ttu-id="65e42-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e42-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65e42-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e42-122">-WhatIf</span></span>
<span data-ttu-id="65e42-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65e42-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65e42-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65e42-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65e42-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e42-125">CommonParameters</span></span>
<span data-ttu-id="65e42-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e42-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e42-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e42-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e42-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65e42-128">INPUTS</span></span>

### <span data-ttu-id="65e42-129">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="65e42-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="65e42-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="65e42-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="65e42-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65e42-131">OUTPUTS</span></span>

### <span data-ttu-id="65e42-132">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="65e42-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="65e42-133">Note</span><span class="sxs-lookup"><span data-stu-id="65e42-133">NOTES</span></span>

## <span data-ttu-id="65e42-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65e42-134">RELATED LINKS</span></span>

