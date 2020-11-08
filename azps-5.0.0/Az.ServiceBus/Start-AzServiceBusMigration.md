---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193827"
---
# <span data-ttu-id="caa00-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="caa00-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="caa00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="caa00-102">SYNOPSIS</span></span>
<span data-ttu-id="caa00-103">Crea una nuova configurazione di migrazione e avvia la migrazione delle entità da standard a spazi dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="caa00-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="caa00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="caa00-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caa00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caa00-105">DESCRIPTION</span></span>
<span data-ttu-id="caa00-106">Il cmdlet **Start-AzServiceBusMigration** crea una nuova configurazione di migrazione e avvia la migrazione delle entità da standard a spazi dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="caa00-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="caa00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="caa00-107">EXAMPLES</span></span>

### <span data-ttu-id="caa00-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="caa00-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="caa00-109">Crea una nuova configurazione di migrazione per gli spazi dei nomi "TestingNamespaceStandardMigration" in "TestingNamespacePremiumMigration"</span><span class="sxs-lookup"><span data-stu-id="caa00-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="caa00-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="caa00-110">PARAMETERS</span></span>

### <span data-ttu-id="caa00-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="caa00-111">-AsJob</span></span>
<span data-ttu-id="caa00-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="caa00-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa00-113">-DefaultProfile</span></span>
<span data-ttu-id="caa00-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="caa00-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caa00-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="caa00-115">-Name</span></span>
<span data-ttu-id="caa00-116">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="caa00-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa00-117">-Postmigrationname</span><span class="sxs-lookup"><span data-stu-id="caa00-117">-PostMigrationName</span></span>
<span data-ttu-id="caa00-118">Pubblicare il nome della migrazione per lo spazio dei nomi standard nella migrazione</span><span class="sxs-lookup"><span data-stu-id="caa00-118">Post Migration Name for Standard Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caa00-119">-ResourceGroupName</span></span>
<span data-ttu-id="caa00-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="caa00-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa00-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="caa00-121">-TargetNameSpace</span></span>
<span data-ttu-id="caa00-122">ID ARM dello spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="caa00-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa00-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="caa00-123">-Confirm</span></span>
<span data-ttu-id="caa00-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caa00-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa00-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa00-125">-WhatIf</span></span>
<span data-ttu-id="caa00-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="caa00-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caa00-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="caa00-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa00-128">CommonParameters</span></span>
<span data-ttu-id="caa00-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caa00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa00-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa00-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa00-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="caa00-131">INPUTS</span></span>

### <span data-ttu-id="caa00-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="caa00-132">None</span></span>

## <span data-ttu-id="caa00-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="caa00-133">OUTPUTS</span></span>

### <span data-ttu-id="caa00-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="caa00-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="caa00-135">Note</span><span class="sxs-lookup"><span data-stu-id="caa00-135">NOTES</span></span>

## <span data-ttu-id="caa00-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="caa00-136">RELATED LINKS</span></span>
