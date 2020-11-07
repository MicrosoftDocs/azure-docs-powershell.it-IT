---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 87786196e027597dc532bcaab2adfec4aa8c3892
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863434"
---
# <span data-ttu-id="d0388-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="d0388-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="d0388-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0388-102">SYNOPSIS</span></span>
<span data-ttu-id="d0388-103">Imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="d0388-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="d0388-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0388-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0388-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0388-105">DESCRIPTION</span></span>
<span data-ttu-id="d0388-106">Il cmdlet **set-AzSnapshotImageReference** imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="d0388-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="d0388-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0388-107">EXAMPLES</span></span>

### <span data-ttu-id="d0388-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0388-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="d0388-109">Il primo comando crea un oggetto snapshot locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0388-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d0388-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d0388-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="d0388-111">Il secondo comando imposta l'ID immagine e il numero di unità logica 0 per lo snapshot Obejct.</span><span class="sxs-lookup"><span data-stu-id="d0388-111">The second command sets the image ID and the logical unit number 0 for the snapshot obejct.</span></span>
<span data-ttu-id="d0388-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d0388-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d0388-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0388-113">PARAMETERS</span></span>

### <span data-ttu-id="d0388-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0388-114">-DefaultProfile</span></span>
<span data-ttu-id="d0388-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0388-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0388-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d0388-116">-Id</span></span>
<span data-ttu-id="d0388-117">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="d0388-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="d0388-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="d0388-118">-Lun</span></span>
<span data-ttu-id="d0388-119">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="d0388-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="d0388-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="d0388-120">-Snapshot</span></span>
<span data-ttu-id="d0388-121">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="d0388-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0388-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0388-122">-Confirm</span></span>
<span data-ttu-id="d0388-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0388-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0388-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0388-124">-WhatIf</span></span>
<span data-ttu-id="d0388-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0388-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0388-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0388-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0388-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0388-127">CommonParameters</span></span>
<span data-ttu-id="d0388-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0388-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0388-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0388-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0388-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0388-130">INPUTS</span></span>

### <span data-ttu-id="d0388-131">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="d0388-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="d0388-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d0388-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d0388-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0388-133">OUTPUTS</span></span>

### <span data-ttu-id="d0388-134">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="d0388-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="d0388-135">Note</span><span class="sxs-lookup"><span data-stu-id="d0388-135">NOTES</span></span>

## <span data-ttu-id="d0388-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0388-136">RELATED LINKS</span></span>

