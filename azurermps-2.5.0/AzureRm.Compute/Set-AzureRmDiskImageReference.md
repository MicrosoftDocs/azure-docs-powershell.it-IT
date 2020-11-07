---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866542"
---
# <span data-ttu-id="e631c-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="e631c-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="e631c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e631c-102">SYNOPSIS</span></span>
<span data-ttu-id="e631c-103">Imposta le proprietà di riferimento dell'immagine in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="e631c-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e631c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e631c-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e631c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e631c-105">DESCRIPTION</span></span>
<span data-ttu-id="e631c-106">Il cmdlet **set-AzureRmDiskImageReference** imposta le proprietà di riferimento dell'immagine su un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="e631c-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="e631c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e631c-107">EXAMPLES</span></span>

### <span data-ttu-id="e631c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e631c-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e631c-109">Il primo comando crea un oggetto disco locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e631c-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e631c-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="e631c-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="e631c-111">Il secondo comando imposta l'ID immagine e l'unità logica numero 0 per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="e631c-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="e631c-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e631c-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e631c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e631c-113">PARAMETERS</span></span>

### <span data-ttu-id="e631c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e631c-114">-DefaultProfile</span></span>
<span data-ttu-id="e631c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e631c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e631c-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="e631c-116">-Disk</span></span>
<span data-ttu-id="e631c-117">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="e631c-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="e631c-118">-ID</span><span class="sxs-lookup"><span data-stu-id="e631c-118">-Id</span></span>
<span data-ttu-id="e631c-119">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="e631c-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="e631c-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="e631c-120">-Lun</span></span>
<span data-ttu-id="e631c-121">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="e631c-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="e631c-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e631c-122">-Confirm</span></span>
<span data-ttu-id="e631c-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e631c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e631c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e631c-124">-WhatIf</span></span>
<span data-ttu-id="e631c-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e631c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e631c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e631c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e631c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e631c-127">CommonParameters</span></span>
<span data-ttu-id="e631c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e631c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e631c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e631c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e631c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e631c-130">INPUTS</span></span>

### <span data-ttu-id="e631c-131">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="e631c-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="e631c-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e631c-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e631c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e631c-133">OUTPUTS</span></span>

### <span data-ttu-id="e631c-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="e631c-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="e631c-135">Note</span><span class="sxs-lookup"><span data-stu-id="e631c-135">NOTES</span></span>

## <span data-ttu-id="e631c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e631c-136">RELATED LINKS</span></span>

