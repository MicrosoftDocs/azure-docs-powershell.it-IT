---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 1d298a543071c879e2279734247febba00b8da21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508051"
---
# <span data-ttu-id="07d3f-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="07d3f-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="07d3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="07d3f-103">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="07d3f-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07d3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07d3f-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07d3f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="07d3f-106">Il cmdlet **New-AzureRmRecoveryServicesAsrvCenter** aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="07d3f-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="07d3f-107">Questo cmdlet registra il server vCenter per l'individuazione con il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="07d3f-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="07d3f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07d3f-108">EXAMPLES</span></span>

### <span data-ttu-id="07d3f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07d3f-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="07d3f-110">Aggiunge un server vCenter per individuare gli elementi protetti.</span><span class="sxs-lookup"><span data-stu-id="07d3f-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="07d3f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07d3f-111">PARAMETERS</span></span>

### <span data-ttu-id="07d3f-112">-Account</span><span class="sxs-lookup"><span data-stu-id="07d3f-112">-Account</span></span>
<span data-ttu-id="07d3f-113">Account di accesso utente di creadential.</span><span class="sxs-lookup"><span data-stu-id="07d3f-113">User login creadential Account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07d3f-114">-Confirm</span></span>
<span data-ttu-id="07d3f-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07d3f-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d3f-116">-DefaultProfile</span></span>
<span data-ttu-id="07d3f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07d3f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-118">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="07d3f-118">-Fabric</span></span>
<span data-ttu-id="07d3f-119">Tessuto ASR corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="07d3f-119">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-120">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="07d3f-120">-IpOrHostName</span></span>
<span data-ttu-id="07d3f-121">Indirizzo IPv4 o FQDN del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="07d3f-121">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="07d3f-122">-Name</span></span>
<span data-ttu-id="07d3f-123">Un nome descrittivo per il server vCenter.</span><span class="sxs-lookup"><span data-stu-id="07d3f-123">A friendly name for the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-124">-Porta</span><span class="sxs-lookup"><span data-stu-id="07d3f-124">-Port</span></span>
<span data-ttu-id="07d3f-125">Porta TCP sul server vCenter da usare per l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="07d3f-125">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07d3f-126">-WhatIf</span></span>
<span data-ttu-id="07d3f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07d3f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07d3f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07d3f-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d3f-129">CommonParameters</span></span>
<span data-ttu-id="07d3f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d3f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d3f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d3f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d3f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07d3f-132">INPUTS</span></span>

### <span data-ttu-id="07d3f-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="07d3f-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="07d3f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07d3f-134">OUTPUTS</span></span>

### <span data-ttu-id="07d3f-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="07d3f-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="07d3f-136">Note</span><span class="sxs-lookup"><span data-stu-id="07d3f-136">NOTES</span></span>

## <span data-ttu-id="07d3f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07d3f-137">RELATED LINKS</span></span>
