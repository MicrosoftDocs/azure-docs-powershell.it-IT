---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: bbaa82500e06f426dd5b7496849507b91a599da6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685736"
---
# <span data-ttu-id="1433d-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="1433d-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="1433d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1433d-102">SYNOPSIS</span></span>
<span data-ttu-id="1433d-103">Imposta le proprietà di riferimento dell'immagine in un oggetto Update snapshot.</span><span class="sxs-lookup"><span data-stu-id="1433d-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1433d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1433d-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <PSSnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1433d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1433d-105">DESCRIPTION</span></span>
<span data-ttu-id="1433d-106">Il cmdlet **set-AzureRmSnapshotUpdateImageReference** imposta le proprietà di riferimento dell'immagine in un oggetto Update snapshot.</span><span class="sxs-lookup"><span data-stu-id="1433d-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="1433d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1433d-107">EXAMPLES</span></span>

### <span data-ttu-id="1433d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1433d-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="1433d-109">Il primo comando crea un oggetto aggiornamento snapshot locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1433d-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="1433d-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="1433d-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="1433d-111">Il secondo comando imposta l'ID immagine e il numero di unità logica 0 per l'oggetto aggiornamento snapshot.</span><span class="sxs-lookup"><span data-stu-id="1433d-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="1433d-112">L'ultimo comando accetta l'oggetto Update dello snapshot e aggiorna uno snapshot esistente con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1433d-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1433d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1433d-113">PARAMETERS</span></span>

### <span data-ttu-id="1433d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1433d-114">-DefaultProfile</span></span>
<span data-ttu-id="1433d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1433d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1433d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="1433d-116">-Id</span></span>
<span data-ttu-id="1433d-117">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="1433d-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="1433d-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="1433d-118">-Lun</span></span>
<span data-ttu-id="1433d-119">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="1433d-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="1433d-120">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1433d-120">-SnapshotUpdate</span></span>
<span data-ttu-id="1433d-121">Specifica un oggetto di aggiornamento snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="1433d-121">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1433d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1433d-122">-Confirm</span></span>
<span data-ttu-id="1433d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1433d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1433d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1433d-124">-WhatIf</span></span>
<span data-ttu-id="1433d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1433d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1433d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1433d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1433d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1433d-127">CommonParameters</span></span>
<span data-ttu-id="1433d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1433d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1433d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1433d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1433d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1433d-130">INPUTS</span></span>

### <span data-ttu-id="1433d-131">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1433d-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="1433d-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1433d-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1433d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1433d-133">OUTPUTS</span></span>

### <span data-ttu-id="1433d-134">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1433d-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="1433d-135">Note</span><span class="sxs-lookup"><span data-stu-id="1433d-135">NOTES</span></span>

## <span data-ttu-id="1433d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1433d-136">RELATED LINKS</span></span>

