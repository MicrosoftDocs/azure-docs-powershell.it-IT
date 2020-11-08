---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029679"
---
# <span data-ttu-id="c7bec-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7bec-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="c7bec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7bec-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bec-103">Crea un mapping tra reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="c7bec-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="c7bec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7bec-104">SYNTAX</span></span>

### <span data-ttu-id="c7bec-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c7bec-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c7bec-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c7bec-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7bec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7bec-107">DESCRIPTION</span></span>
<span data-ttu-id="c7bec-108">Il cmdlet **New-AzureSiteRecoveryNetworkMapping** crea un mapping tra due reti virtuali e restituisce un processo di ripristino del sito di Azure per monitorarlo.</span><span class="sxs-lookup"><span data-stu-id="c7bec-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="c7bec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7bec-109">EXAMPLES</span></span>

### <span data-ttu-id="c7bec-110">Esempio 1: creare un mapping tra una rete e una rete di ripristino</span><span class="sxs-lookup"><span data-stu-id="c7bec-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="c7bec-111">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="c7bec-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="c7bec-112">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="c7bec-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="c7bec-113">Il secondo comando ottiene la rete di ripristino del sito per il primo server nella matrice $Servers usando il cmdlet **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="c7bec-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="c7bec-114">Il comando Archivia le reti nella variabile $Networks.</span><span class="sxs-lookup"><span data-stu-id="c7bec-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="c7bec-115">Il comando finale crea un mapping tra la rete principale e la rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c7bec-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="c7bec-116">Il comando specifica la rete principale come primo elemento di $Networks.</span><span class="sxs-lookup"><span data-stu-id="c7bec-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="c7bec-117">Il comando specifica la rete di ripristino come secondo elemento di $Networks.</span><span class="sxs-lookup"><span data-stu-id="c7bec-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="c7bec-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7bec-118">PARAMETERS</span></span>

### <span data-ttu-id="c7bec-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7bec-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="c7bec-120">Specifica l'ID dell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bec-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bec-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c7bec-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="c7bec-122">Specifica l'ID rete virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bec-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bec-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c7bec-123">-PrimaryNetwork</span></span>
<span data-ttu-id="c7bec-124">Specifica l'oggetto di rete principale.</span><span class="sxs-lookup"><span data-stu-id="c7bec-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bec-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="c7bec-125">-Profile</span></span>
<span data-ttu-id="c7bec-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7bec-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7bec-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c7bec-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7bec-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c7bec-128">-RecoveryNetwork</span></span>
<span data-ttu-id="c7bec-129">Specifica l'oggetto rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c7bec-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bec-130">CommonParameters</span></span>
<span data-ttu-id="c7bec-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7bec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bec-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7bec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bec-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7bec-133">INPUTS</span></span>

## <span data-ttu-id="c7bec-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7bec-134">OUTPUTS</span></span>

## <span data-ttu-id="c7bec-135">Note</span><span class="sxs-lookup"><span data-stu-id="c7bec-135">NOTES</span></span>

## <span data-ttu-id="c7bec-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7bec-136">RELATED LINKS</span></span>

[<span data-ttu-id="c7bec-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7bec-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="c7bec-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="c7bec-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="c7bec-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7bec-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


