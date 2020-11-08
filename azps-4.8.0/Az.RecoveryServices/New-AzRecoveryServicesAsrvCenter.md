---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c821437a128dc6ede02d1bccc8cf409e152c217c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192219"
---
# <span data-ttu-id="31e25-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="31e25-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="31e25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31e25-102">SYNOPSIS</span></span>
<span data-ttu-id="31e25-103">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="31e25-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="31e25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31e25-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e25-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31e25-105">DESCRIPTION</span></span>
<span data-ttu-id="31e25-106">Il cmdlet **New-AzRecoveryServicesAsrvCenter** aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="31e25-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="31e25-107">Questo cmdlet registra il server vCenter per l'individuazione con il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="31e25-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="31e25-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31e25-108">EXAMPLES</span></span>

### <span data-ttu-id="31e25-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31e25-109">Example 1</span></span>
```powershell
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="31e25-110">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="31e25-110">Adds a vCenter server to discover protectable items from.</span></span>

### <span data-ttu-id="31e25-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="31e25-111">Example 2</span></span>

<span data-ttu-id="31e25-112">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="31e25-112">Adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="31e25-113">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="31e25-113">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrvCenter -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -Fabric $Fabric -IpOrHostName <String> -Name 'V2VM' -Port <Int32>
```

## <span data-ttu-id="31e25-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31e25-114">PARAMETERS</span></span>

### <span data-ttu-id="31e25-115">-Account</span><span class="sxs-lookup"><span data-stu-id="31e25-115">-Account</span></span>
<span data-ttu-id="31e25-116">Account delle credenziali di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="31e25-116">User login credential Account.</span></span>

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

### <span data-ttu-id="31e25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e25-117">-DefaultProfile</span></span>
<span data-ttu-id="31e25-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31e25-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e25-119">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="31e25-119">-Fabric</span></span>
<span data-ttu-id="31e25-120">Tessuto ASR corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="31e25-120">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="31e25-121">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="31e25-121">-IpOrHostName</span></span>
<span data-ttu-id="31e25-122">Indirizzo IPv4 o FQDN del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="31e25-122">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="31e25-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="31e25-123">-Name</span></span>
<span data-ttu-id="31e25-124">Un nome descrittivo per il server vCenter.</span><span class="sxs-lookup"><span data-stu-id="31e25-124">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="31e25-125">-Porta</span><span class="sxs-lookup"><span data-stu-id="31e25-125">-Port</span></span>
<span data-ttu-id="31e25-126">Porta TCP sul server vCenter da usare per l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="31e25-126">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="31e25-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31e25-127">-Confirm</span></span>
<span data-ttu-id="31e25-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e25-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e25-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e25-129">-WhatIf</span></span>
<span data-ttu-id="31e25-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e25-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e25-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e25-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e25-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e25-132">CommonParameters</span></span>
<span data-ttu-id="31e25-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e25-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e25-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31e25-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e25-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31e25-135">INPUTS</span></span>

### <span data-ttu-id="31e25-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="31e25-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="31e25-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31e25-137">OUTPUTS</span></span>

### <span data-ttu-id="31e25-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="31e25-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="31e25-139">Note</span><span class="sxs-lookup"><span data-stu-id="31e25-139">NOTES</span></span>

## <span data-ttu-id="31e25-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31e25-140">RELATED LINKS</span></span>