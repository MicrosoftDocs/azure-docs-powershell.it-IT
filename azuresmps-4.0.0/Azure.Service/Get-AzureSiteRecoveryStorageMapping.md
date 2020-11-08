---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023533"
---
# <span data-ttu-id="66de1-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="66de1-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="66de1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66de1-102">SYNOPSIS</span></span>
<span data-ttu-id="66de1-103">Ottiene i mapping degli oggetti di archiviazione del ripristino del sito per un Vault.</span><span class="sxs-lookup"><span data-stu-id="66de1-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="66de1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66de1-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66de1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66de1-105">DESCRIPTION</span></span>
<span data-ttu-id="66de1-106">Il cmdlet **Get-AzureSiteRecoveryStorageMapping** ottiene i mapping degli oggetti di archiviazione di ripristino del sito di Azure per il Vault di ripristino del sito Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="66de1-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="66de1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66de1-107">EXAMPLES</span></span>

### <span data-ttu-id="66de1-108">Esempio 1: ottenere il mapping tra un oggetto di archiviazione e un oggetto di archiviazione di ripristino</span><span class="sxs-lookup"><span data-stu-id="66de1-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="66de1-109">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="66de1-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="66de1-110">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="66de1-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="66de1-111">Il secondo comando ottiene il mapping tra due oggetti di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="66de1-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="66de1-112">Il comando specifica il server primario per il mapping degli oggetti di archiviazione come primo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="66de1-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="66de1-113">Il comando specifica il server per l'oggetto di archiviazione di ripristino come secondo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="66de1-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="66de1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66de1-114">PARAMETERS</span></span>

### <span data-ttu-id="66de1-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="66de1-115">-PrimaryServer</span></span>
<span data-ttu-id="66de1-116">Specifica il server primario.</span><span class="sxs-lookup"><span data-stu-id="66de1-116">Specifies the primary server.</span></span>
<span data-ttu-id="66de1-117">Per ottenere un server, usare il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="66de1-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66de1-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="66de1-118">-Profile</span></span>
<span data-ttu-id="66de1-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66de1-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66de1-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="66de1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66de1-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="66de1-121">-RecoveryServer</span></span>
<span data-ttu-id="66de1-122">Specifica il server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="66de1-122">Specifies the recovery server.</span></span>
<span data-ttu-id="66de1-123">Per ottenere un server, USA **Get-AzureSiteRecoveryServer**.</span><span class="sxs-lookup"><span data-stu-id="66de1-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66de1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66de1-124">CommonParameters</span></span>
<span data-ttu-id="66de1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66de1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66de1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66de1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66de1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66de1-127">INPUTS</span></span>

## <span data-ttu-id="66de1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66de1-128">OUTPUTS</span></span>

## <span data-ttu-id="66de1-129">Note</span><span class="sxs-lookup"><span data-stu-id="66de1-129">NOTES</span></span>

## <span data-ttu-id="66de1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66de1-130">RELATED LINKS</span></span>

[<span data-ttu-id="66de1-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="66de1-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="66de1-132">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="66de1-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="66de1-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="66de1-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


