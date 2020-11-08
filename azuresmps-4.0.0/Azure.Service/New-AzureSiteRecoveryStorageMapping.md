---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023933"
---
# <span data-ttu-id="3d8f2-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="3d8f2-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="3d8f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8f2-103">Crea un mapping tra un oggetto di archiviazione di Azure e un oggetto di archiviazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="3d8f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d8f2-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d8f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d8f2-105">DESCRIPTION</span></span>
<span data-ttu-id="3d8f2-106">Il cmdlet **New-AzureSiteRecoveryStorageMapping** crea un mapping tra un oggetto di archiviazione di Azure primaria gestito e un oggetto di archiviazione di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="3d8f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d8f2-107">EXAMPLES</span></span>

### <span data-ttu-id="3d8f2-108">Esempio 1: creare un mapping tra un oggetto di archiviazione e un oggetto di archiviazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="3d8f2-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="3d8f2-109">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="3d8f2-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="3d8f2-110">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="3d8f2-111">Il secondo comando consente di ottenere l'archiviazione di ripristino del sito per il primo server nella matrice $Servers e quindi di archiviarla nel $Storages.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="3d8f2-112">Il comando finale crea un mapping tra la rete principale e la rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="3d8f2-113">Il comando specifica l'oggetto di archiviazione principale come primo elemento di $Storages.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="3d8f2-114">Il comando specifica l'oggetto di archiviazione di ripristino come secondo elemento di $Storages.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="3d8f2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d8f2-115">PARAMETERS</span></span>

### <span data-ttu-id="3d8f2-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="3d8f2-116">-PrimaryStorage</span></span>
<span data-ttu-id="3d8f2-117">Specifica lo spazio di archiviazione principale da associare all'archivio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="3d8f2-118">Per ottenere un oggetto **ASRStorage** , usa il cmdlet Get-AzureSiteRecoveryStorage.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8f2-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d8f2-119">-Profile</span></span>
<span data-ttu-id="3d8f2-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d8f2-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8f2-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="3d8f2-122">-RecoveryStorage</span></span>
<span data-ttu-id="3d8f2-123">Specifica l'oggetto di archiviazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="3d8f2-124">Questo cmdlet associa l'oggetto di archiviazione principale all'oggetto di archiviazione specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="3d8f2-125">Per ottenere un oggetto **ASRStorage** , USA **Get-AzureSiteRecoveryStorage**.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8f2-126">CommonParameters</span></span>
<span data-ttu-id="3d8f2-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d8f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8f2-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d8f2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8f2-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d8f2-129">INPUTS</span></span>

## <span data-ttu-id="3d8f2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d8f2-130">OUTPUTS</span></span>

## <span data-ttu-id="3d8f2-131">Note</span><span class="sxs-lookup"><span data-stu-id="3d8f2-131">NOTES</span></span>

## <span data-ttu-id="3d8f2-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d8f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="3d8f2-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="3d8f2-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="3d8f2-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="3d8f2-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="3d8f2-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="3d8f2-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


