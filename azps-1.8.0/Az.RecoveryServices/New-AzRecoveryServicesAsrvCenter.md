---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 98bc2dfde30357e7f6a3db62ec550a2a0c173bb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677616"
---
# <span data-ttu-id="ee3da-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="ee3da-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="ee3da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee3da-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3da-103">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="ee3da-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="ee3da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee3da-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee3da-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee3da-105">DESCRIPTION</span></span>
<span data-ttu-id="ee3da-106">Il cmdlet **New-AzRecoveryServicesAsrvCenter** aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="ee3da-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="ee3da-107">Questo cmdlet registra il server vCenter per l'individuazione con il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="ee3da-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="ee3da-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee3da-108">EXAMPLES</span></span>

### <span data-ttu-id="ee3da-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee3da-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="ee3da-110">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="ee3da-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="ee3da-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee3da-111">PARAMETERS</span></span>

### <span data-ttu-id="ee3da-112">-Account</span><span class="sxs-lookup"><span data-stu-id="ee3da-112">-Account</span></span>
<span data-ttu-id="ee3da-113">Account di accesso utente di creadential.</span><span class="sxs-lookup"><span data-stu-id="ee3da-113">User login creadential Account.</span></span>

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

### <span data-ttu-id="ee3da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3da-114">-DefaultProfile</span></span>
<span data-ttu-id="ee3da-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3da-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee3da-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="ee3da-116">-Fabric</span></span>
<span data-ttu-id="ee3da-117">Tessuto ASR corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="ee3da-117">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="ee3da-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="ee3da-118">-IpOrHostName</span></span>
<span data-ttu-id="ee3da-119">Indirizzo IPv4 o FQDN del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="ee3da-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="ee3da-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee3da-120">-Name</span></span>
<span data-ttu-id="ee3da-121">Un nome descrittivo per il server vCenter.</span><span class="sxs-lookup"><span data-stu-id="ee3da-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="ee3da-122">-Porta</span><span class="sxs-lookup"><span data-stu-id="ee3da-122">-Port</span></span>
<span data-ttu-id="ee3da-123">Porta TCP sul server vCenter da usare per l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="ee3da-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="ee3da-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee3da-124">-Confirm</span></span>
<span data-ttu-id="ee3da-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee3da-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee3da-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee3da-126">-WhatIf</span></span>
<span data-ttu-id="ee3da-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee3da-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee3da-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee3da-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee3da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3da-129">CommonParameters</span></span>
<span data-ttu-id="ee3da-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3da-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee3da-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3da-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee3da-132">INPUTS</span></span>

### <span data-ttu-id="ee3da-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ee3da-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ee3da-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee3da-134">OUTPUTS</span></span>

### <span data-ttu-id="ee3da-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ee3da-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ee3da-136">Note</span><span class="sxs-lookup"><span data-stu-id="ee3da-136">NOTES</span></span>

## <span data-ttu-id="ee3da-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee3da-137">RELATED LINKS</span></span>
