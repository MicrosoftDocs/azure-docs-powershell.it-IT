---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: c27d4d88dd4c2fdf86db5ca39d608add2feb845f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507344"
---
# <span data-ttu-id="2fd36-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="2fd36-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="2fd36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fd36-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd36-103">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="2fd36-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fd36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fd36-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fd36-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fd36-105">DESCRIPTION</span></span>
<span data-ttu-id="2fd36-106">Il cmdlet **New-AzureRmRecoveryServicesAsrvCenter** aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="2fd36-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="2fd36-107">Questo cmdlet registra il server vCenter per l'individuazione con il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2fd36-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="2fd36-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fd36-108">EXAMPLES</span></span>

### <span data-ttu-id="2fd36-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2fd36-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="2fd36-110">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="2fd36-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="2fd36-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fd36-111">PARAMETERS</span></span>

### <span data-ttu-id="2fd36-112">-Account</span><span class="sxs-lookup"><span data-stu-id="2fd36-112">-Account</span></span>
<span data-ttu-id="2fd36-113">Account di accesso utente di creadential.</span><span class="sxs-lookup"><span data-stu-id="2fd36-113">User login creadential Account.</span></span>

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

### <span data-ttu-id="2fd36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd36-114">-DefaultProfile</span></span>
<span data-ttu-id="2fd36-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fd36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd36-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="2fd36-116">-Fabric</span></span>
<span data-ttu-id="2fd36-117">Tessuto ASR corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2fd36-117">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="2fd36-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="2fd36-118">-IpOrHostName</span></span>
<span data-ttu-id="2fd36-119">Indirizzo IPv4 o FQDN del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="2fd36-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="2fd36-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fd36-120">-Name</span></span>
<span data-ttu-id="2fd36-121">Un nome descrittivo per il server vCenter.</span><span class="sxs-lookup"><span data-stu-id="2fd36-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="2fd36-122">-Porta</span><span class="sxs-lookup"><span data-stu-id="2fd36-122">-Port</span></span>
<span data-ttu-id="2fd36-123">Porta TCP sul server vCenter da usare per l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="2fd36-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="2fd36-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2fd36-124">-Confirm</span></span>
<span data-ttu-id="2fd36-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fd36-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd36-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd36-126">-WhatIf</span></span>
<span data-ttu-id="2fd36-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fd36-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd36-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fd36-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd36-129">CommonParameters</span></span>
<span data-ttu-id="2fd36-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fd36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd36-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd36-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd36-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fd36-132">INPUTS</span></span>

### <span data-ttu-id="2fd36-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2fd36-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2fd36-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fd36-134">OUTPUTS</span></span>

### <span data-ttu-id="2fd36-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2fd36-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2fd36-136">Note</span><span class="sxs-lookup"><span data-stu-id="2fd36-136">NOTES</span></span>

## <span data-ttu-id="2fd36-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fd36-137">RELATED LINKS</span></span>
