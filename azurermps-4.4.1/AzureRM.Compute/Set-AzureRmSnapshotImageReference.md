---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: b88802503247b1e753c9363558df30e57079f897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520785"
---
# <span data-ttu-id="c8f06-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="c8f06-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="c8f06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8f06-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f06-103">Imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="c8f06-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8f06-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8f06-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f06-106">Il cmdlet **set-AzureRmSnapshotImageReference** imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="c8f06-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="c8f06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8f06-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f06-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8f06-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="c8f06-109">Il primo comando crea un oggetto snapshot locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c8f06-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="c8f06-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="c8f06-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="c8f06-111">Il secondo comando imposta l'ID immagine e il numero di unità logica 0 per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="c8f06-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="c8f06-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c8f06-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c8f06-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8f06-113">PARAMETERS</span></span>

### <span data-ttu-id="c8f06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f06-114">-DefaultProfile</span></span>
<span data-ttu-id="c8f06-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f06-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8f06-116">-ID</span><span class="sxs-lookup"><span data-stu-id="c8f06-116">-Id</span></span>
<span data-ttu-id="c8f06-117">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="c8f06-117">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8f06-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="c8f06-118">-Lun</span></span>
<span data-ttu-id="c8f06-119">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="c8f06-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8f06-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="c8f06-120">-Snapshot</span></span>
<span data-ttu-id="c8f06-121">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="c8f06-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8f06-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8f06-122">-Confirm</span></span>
<span data-ttu-id="c8f06-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8f06-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8f06-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f06-124">-WhatIf</span></span>
<span data-ttu-id="c8f06-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8f06-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8f06-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8f06-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8f06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f06-127">CommonParameters</span></span>
<span data-ttu-id="c8f06-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f06-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f06-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f06-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8f06-130">INPUTS</span></span>

### <span data-ttu-id="c8f06-131">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="c8f06-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="c8f06-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c8f06-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c8f06-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8f06-133">OUTPUTS</span></span>

### <span data-ttu-id="c8f06-134">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="c8f06-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="c8f06-135">Note</span><span class="sxs-lookup"><span data-stu-id="c8f06-135">NOTES</span></span>

## <span data-ttu-id="c8f06-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8f06-136">RELATED LINKS</span></span>

