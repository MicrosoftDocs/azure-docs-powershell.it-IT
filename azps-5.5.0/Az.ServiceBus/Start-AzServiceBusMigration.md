---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208099"
---
# <span data-ttu-id="d9bb1-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d9bb1-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="d9bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bb1-103">Crea una nuova configurazione di migrazione e inizia la migrazione delle entità dagli spazi dei nomi Standard a Premium</span><span class="sxs-lookup"><span data-stu-id="d9bb1-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="d9bb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9bb1-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9bb1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bb1-106">Il cmdlet **Start-AzServiceBusMigration** crea una nuova configurazione di migrazione e inizia la migrazione delle entità dagli spazi dei nomi Standard a Premium</span><span class="sxs-lookup"><span data-stu-id="d9bb1-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="d9bb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bb1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9bb1-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="d9bb1-109">Crea una nuova configurazione di migrazione per 'TestingStandardMigration' agli spazi dei nomi 'TestingNapPremiumMigration'</span><span class="sxs-lookup"><span data-stu-id="d9bb1-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="d9bb1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9bb1-110">PARAMETERS</span></span>

### <span data-ttu-id="d9bb1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9bb1-111">-AsJob</span></span>
<span data-ttu-id="d9bb1-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9bb1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9bb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bb1-113">-DefaultProfile</span></span>
<span data-ttu-id="d9bb1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9bb1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9bb1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d9bb1-115">-Name</span></span>
<span data-ttu-id="d9bb1-116">Nome spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="d9bb1-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="d9bb1-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="d9bb1-117">-PostMigrationName</span></span>
<span data-ttu-id="d9bb1-118">Nome post-migrazione per lo spazio dei nomi standard nella migrazione</span><span class="sxs-lookup"><span data-stu-id="d9bb1-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="d9bb1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bb1-119">-ResourceGroupName</span></span>
<span data-ttu-id="d9bb1-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d9bb1-120">Resource Group Name</span></span>

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

### <span data-ttu-id="d9bb1-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="d9bb1-121">-TargetNameSpace</span></span>
<span data-ttu-id="d9bb1-122">ID dell'ARM Premium</span><span class="sxs-lookup"><span data-stu-id="d9bb1-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="d9bb1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9bb1-123">-Confirm</span></span>
<span data-ttu-id="d9bb1-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9bb1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bb1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bb1-125">-WhatIf</span></span>
<span data-ttu-id="d9bb1-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9bb1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bb1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9bb1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bb1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bb1-128">CommonParameters</span></span>
<span data-ttu-id="d9bb1-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bb1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bb1-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9bb1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bb1-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9bb1-131">INPUTS</span></span>

### <span data-ttu-id="d9bb1-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9bb1-132">None</span></span>

## <span data-ttu-id="d9bb1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9bb1-133">OUTPUTS</span></span>

### <span data-ttu-id="d9bb1-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d9bb1-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="d9bb1-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9bb1-135">NOTES</span></span>

## <span data-ttu-id="d9bb1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9bb1-136">RELATED LINKS</span></span>
