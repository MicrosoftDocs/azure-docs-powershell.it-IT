---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 010e54b21d4abb3068f62e561c002fed6ca734d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988804"
---
# <span data-ttu-id="05500-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="05500-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="05500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05500-102">SYNOPSIS</span></span>
<span data-ttu-id="05500-103">Crea una nuova configurazione di migrazione e inizia la migrazione delle entità dagli spazi dei nomi Standard a Premium</span><span class="sxs-lookup"><span data-stu-id="05500-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="05500-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05500-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05500-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05500-105">DESCRIPTION</span></span>
<span data-ttu-id="05500-106">Il cmdlet **Start-AzServiceBusMigration** crea una nuova configurazione di migrazione e inizia la migrazione delle entità dagli spazi dei nomi Standard a Premium</span><span class="sxs-lookup"><span data-stu-id="05500-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="05500-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05500-107">EXAMPLES</span></span>

### <span data-ttu-id="05500-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05500-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="05500-109">Crea una nuova configurazione di migrazione per 'TestingStandardMigration' per gli spazi dei nomi 'TestingStandardPremiumMigration'</span><span class="sxs-lookup"><span data-stu-id="05500-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="05500-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05500-110">PARAMETERS</span></span>

### <span data-ttu-id="05500-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05500-111">-AsJob</span></span>
<span data-ttu-id="05500-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="05500-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05500-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05500-113">-DefaultProfile</span></span>
<span data-ttu-id="05500-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05500-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05500-115">-Name</span><span class="sxs-lookup"><span data-stu-id="05500-115">-Name</span></span>
<span data-ttu-id="05500-116">Nome spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="05500-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="05500-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="05500-117">-PostMigrationName</span></span>
<span data-ttu-id="05500-118">Nome post-migrazione per lo spazio dei nomi standard nella migrazione</span><span class="sxs-lookup"><span data-stu-id="05500-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="05500-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05500-119">-ResourceGroupName</span></span>
<span data-ttu-id="05500-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="05500-120">Resource Group Name</span></span>

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

### <span data-ttu-id="05500-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="05500-121">-TargetNameSpace</span></span>
<span data-ttu-id="05500-122">ID dell'ARM Premium</span><span class="sxs-lookup"><span data-stu-id="05500-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="05500-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05500-123">-Confirm</span></span>
<span data-ttu-id="05500-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05500-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05500-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05500-125">-WhatIf</span></span>
<span data-ttu-id="05500-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05500-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05500-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05500-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05500-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05500-128">CommonParameters</span></span>
<span data-ttu-id="05500-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05500-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05500-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05500-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05500-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="05500-131">INPUTS</span></span>

### <span data-ttu-id="05500-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05500-132">None</span></span>

## <span data-ttu-id="05500-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05500-133">OUTPUTS</span></span>

### <span data-ttu-id="05500-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="05500-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="05500-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="05500-135">NOTES</span></span>

## <span data-ttu-id="05500-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05500-136">RELATED LINKS</span></span>
