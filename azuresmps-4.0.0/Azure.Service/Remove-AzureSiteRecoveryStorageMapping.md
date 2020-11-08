---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029571"
---
# <span data-ttu-id="2e386-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="2e386-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="2e386-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e386-102">SYNOPSIS</span></span>
<span data-ttu-id="2e386-103">Rimuove un mapping degli oggetti di archiviazione per un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="2e386-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="2e386-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e386-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e386-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e386-105">DESCRIPTION</span></span>
<span data-ttu-id="2e386-106">Il cmdlet **Remove-AzureSiteRecoveryStorageMapping** rimuove un mapping degli oggetti di archiviazione per il Vault di ripristino di Azure del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="2e386-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2e386-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e386-107">EXAMPLES</span></span>

### <span data-ttu-id="2e386-108">Esempio 1: rimuovere il mapping tra una rete e una rete di ripristino</span><span class="sxs-lookup"><span data-stu-id="2e386-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="2e386-109">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="2e386-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="2e386-110">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="2e386-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="2e386-111">Il secondo comando ottiene il mapping tra due oggetti di archiviazione e lo archivia nella variabile $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="2e386-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="2e386-112">Il comando specifica il server primario per il mapping di rete come primo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="2e386-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="2e386-113">Il comando specifica il server per la rete di ripristino come secondo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="2e386-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="2e386-114">Il comando finale rimuove il mapping in $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="2e386-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="2e386-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e386-115">PARAMETERS</span></span>

### <span data-ttu-id="2e386-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="2e386-116">-Profile</span></span>
<span data-ttu-id="2e386-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e386-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e386-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2e386-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e386-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="2e386-119">-StorageMapping</span></span>
<span data-ttu-id="2e386-120">Specifica un mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="2e386-120">Specifies a network mapping.</span></span>
<span data-ttu-id="2e386-121">Per ottenere un **ASRStorageMapping** , usare il cmdlet **Get-AzureSiteRecoveryStorage** .</span><span class="sxs-lookup"><span data-stu-id="2e386-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e386-122">CommonParameters</span></span>
<span data-ttu-id="2e386-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e386-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e386-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e386-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e386-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e386-125">INPUTS</span></span>

## <span data-ttu-id="2e386-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e386-126">OUTPUTS</span></span>

## <span data-ttu-id="2e386-127">Note</span><span class="sxs-lookup"><span data-stu-id="2e386-127">NOTES</span></span>

## <span data-ttu-id="2e386-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e386-128">RELATED LINKS</span></span>

[<span data-ttu-id="2e386-129">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="2e386-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


