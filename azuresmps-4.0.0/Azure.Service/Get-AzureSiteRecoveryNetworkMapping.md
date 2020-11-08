---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023548"
---
# <span data-ttu-id="985f3-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="985f3-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="985f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="985f3-102">SYNOPSIS</span></span>
<span data-ttu-id="985f3-103">Ottiene i mapping di rete per un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="985f3-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="985f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="985f3-104">SYNTAX</span></span>

### <span data-ttu-id="985f3-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="985f3-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="985f3-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="985f3-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="985f3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="985f3-107">DESCRIPTION</span></span>
<span data-ttu-id="985f3-108">Il cmdlet **Get-AzureSiteRecoveryNetworkMapping** ottiene le informazioni sui mapping di rete di ripristino dei siti di Azure per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="985f3-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="985f3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="985f3-109">EXAMPLES</span></span>

### <span data-ttu-id="985f3-110">Esempio 1: ottenere il mapping tra una rete e una rete di ripristino</span><span class="sxs-lookup"><span data-stu-id="985f3-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="985f3-111">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="985f3-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="985f3-112">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="985f3-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="985f3-113">Il secondo comando consente di ottenere il mapping tra la rete principale e la rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="985f3-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="985f3-114">Il comando specifica il server primario per il mapping di rete come primo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="985f3-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="985f3-115">Il comando specifica il server per la rete di ripristino come secondo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="985f3-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="985f3-116">Esempio 2: ottenere il mapping tra una rete e una rete di macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="985f3-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="985f3-117">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="985f3-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="985f3-118">Il comando Archivia i server nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="985f3-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="985f3-119">Il secondo comando consente di ottenere un mapping tra la rete principale e una rete di macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="985f3-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="985f3-120">Il comando specifica il server principale per la rete come primo elemento di $Servers.</span><span class="sxs-lookup"><span data-stu-id="985f3-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="985f3-121">Il comando specifica il parametro *Azure* .</span><span class="sxs-lookup"><span data-stu-id="985f3-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="985f3-122">Di conseguenza, il comando ottiene il mapping a una rete di macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="985f3-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="985f3-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="985f3-123">PARAMETERS</span></span>

### <span data-ttu-id="985f3-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="985f3-124">-Azure</span></span>
<span data-ttu-id="985f3-125">Indica che questo cmdlet ottiene i mapping di rete per le reti nel server primario mappato alle reti virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="985f3-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985f3-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="985f3-126">-PrimaryServer</span></span>
<span data-ttu-id="985f3-127">Specifica un server primario per cui ottenere i mapping.</span><span class="sxs-lookup"><span data-stu-id="985f3-127">Specifies a primary server for which to get mappings.</span></span>

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

### <span data-ttu-id="985f3-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="985f3-128">-Profile</span></span>
<span data-ttu-id="985f3-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="985f3-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="985f3-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="985f3-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="985f3-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="985f3-131">-RecoveryServer</span></span>
<span data-ttu-id="985f3-132">Specifica un server di ripristino per cui ottenere i mapping.</span><span class="sxs-lookup"><span data-stu-id="985f3-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="985f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985f3-133">CommonParameters</span></span>
<span data-ttu-id="985f3-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985f3-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="985f3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985f3-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="985f3-136">INPUTS</span></span>

## <span data-ttu-id="985f3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="985f3-137">OUTPUTS</span></span>

## <span data-ttu-id="985f3-138">Note</span><span class="sxs-lookup"><span data-stu-id="985f3-138">NOTES</span></span>

## <span data-ttu-id="985f3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="985f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="985f3-140">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="985f3-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="985f3-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="985f3-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


