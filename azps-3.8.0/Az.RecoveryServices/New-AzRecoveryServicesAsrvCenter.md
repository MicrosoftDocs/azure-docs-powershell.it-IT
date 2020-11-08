---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 696c5812a4b8eece62261208c501727aa48c2262
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020643"
---
# <span data-ttu-id="64766-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="64766-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="64766-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64766-102">SYNOPSIS</span></span>
<span data-ttu-id="64766-103">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="64766-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="64766-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64766-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64766-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64766-105">DESCRIPTION</span></span>
<span data-ttu-id="64766-106">Il cmdlet **New-AzRecoveryServicesAsrvCenter** aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="64766-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="64766-107">Questo cmdlet registra il server vCenter per l'individuazione con il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="64766-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="64766-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64766-108">EXAMPLES</span></span>

### <span data-ttu-id="64766-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64766-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="64766-110">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="64766-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="64766-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64766-111">PARAMETERS</span></span>

### <span data-ttu-id="64766-112">-Account</span><span class="sxs-lookup"><span data-stu-id="64766-112">-Account</span></span>
<span data-ttu-id="64766-113">Account delle credenziali di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64766-113">User login credential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64766-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64766-114">-DefaultProfile</span></span>
<span data-ttu-id="64766-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64766-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64766-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="64766-116">-Fabric</span></span>
<span data-ttu-id="64766-117">Tessuto ASR corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="64766-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64766-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="64766-118">-IpOrHostName</span></span>
<span data-ttu-id="64766-119">Indirizzo IPv4 o FQDN del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="64766-119">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64766-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="64766-120">-Name</span></span>
<span data-ttu-id="64766-121">Un nome descrittivo per il server vCenter.</span><span class="sxs-lookup"><span data-stu-id="64766-121">A friendly name for the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64766-122">-Porta</span><span class="sxs-lookup"><span data-stu-id="64766-122">-Port</span></span>
<span data-ttu-id="64766-123">Porta TCP sul server vCenter da usare per l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="64766-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64766-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64766-124">-Confirm</span></span>
<span data-ttu-id="64766-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64766-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64766-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64766-126">-WhatIf</span></span>
<span data-ttu-id="64766-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64766-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64766-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64766-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64766-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64766-129">CommonParameters</span></span>
<span data-ttu-id="64766-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64766-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64766-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64766-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64766-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64766-132">INPUTS</span></span>

### <span data-ttu-id="64766-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="64766-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="64766-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64766-134">OUTPUTS</span></span>

### <span data-ttu-id="64766-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="64766-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64766-136">Note</span><span class="sxs-lookup"><span data-stu-id="64766-136">NOTES</span></span>

## <span data-ttu-id="64766-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64766-137">RELATED LINKS</span></span>
