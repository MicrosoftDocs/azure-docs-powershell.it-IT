---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029572"
---
# <span data-ttu-id="f80bb-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f80bb-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="f80bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f80bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f80bb-103">Rimuove un mapping di rete da un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="f80bb-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="f80bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f80bb-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f80bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f80bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f80bb-106">Il cmdlet **Remove-AzureSiteRecoveryNetworkMapping** rimuove un mapping di rete dall'archivio di ripristino del sito di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="f80bb-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f80bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f80bb-107">EXAMPLES</span></span>

### <span data-ttu-id="f80bb-108">Esempio 1: rimuovere il mapping tra una rete e una rete di ripristino</span><span class="sxs-lookup"><span data-stu-id="f80bb-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="f80bb-109">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="f80bb-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="f80bb-110">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="f80bb-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="f80bb-111">Il secondo comando ottiene il mapping tra la rete principale e la rete di ripristino e lo archivia nella variabile $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f80bb-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="f80bb-112">Il comando specifica il server primario per il mapping di rete come primo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="f80bb-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="f80bb-113">Il comando specifica il server per la rete di ripristino come secondo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="f80bb-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="f80bb-114">Il comando finale rimuove il mapping di rete in $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f80bb-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="f80bb-115">Esempio 2: rimuovere il mapping tra una rete e una rete di macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="f80bb-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="f80bb-116">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="f80bb-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="f80bb-117">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="f80bb-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="f80bb-118">Il secondo comando ottiene un mapping tra la rete principale e una rete di macchine virtuali di Azure e lo archivia nella variabile $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f80bb-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="f80bb-119">Il comando specifica il server principale per la rete come primo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="f80bb-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="f80bb-120">Il comando specifica il parametro *Azure* .</span><span class="sxs-lookup"><span data-stu-id="f80bb-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="f80bb-121">Di conseguenza, il comando ottiene il mapping a una rete di macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="f80bb-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="f80bb-122">Il comando finale rimuove il mapping di rete in $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="f80bb-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="f80bb-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f80bb-123">PARAMETERS</span></span>

### <span data-ttu-id="f80bb-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f80bb-124">-NetworkMapping</span></span>
<span data-ttu-id="f80bb-125">Specifica il mapping di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f80bb-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f80bb-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="f80bb-126">-Profile</span></span>
<span data-ttu-id="f80bb-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f80bb-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f80bb-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f80bb-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f80bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80bb-129">CommonParameters</span></span>
<span data-ttu-id="f80bb-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f80bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80bb-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f80bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80bb-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f80bb-132">INPUTS</span></span>

## <span data-ttu-id="f80bb-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f80bb-133">OUTPUTS</span></span>

## <span data-ttu-id="f80bb-134">Note</span><span class="sxs-lookup"><span data-stu-id="f80bb-134">NOTES</span></span>

## <span data-ttu-id="f80bb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f80bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="f80bb-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f80bb-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="f80bb-137">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f80bb-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="f80bb-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="f80bb-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


