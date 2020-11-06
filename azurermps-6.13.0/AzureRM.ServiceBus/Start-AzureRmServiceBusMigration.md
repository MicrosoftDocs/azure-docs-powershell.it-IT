---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516472"
---
# <span data-ttu-id="1323a-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1323a-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="1323a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1323a-102">SYNOPSIS</span></span>
<span data-ttu-id="1323a-103">Crea una nuova configurazione di migrazione e avvia la migrazione delle entità da standard a spazi dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="1323a-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1323a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1323a-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1323a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1323a-105">DESCRIPTION</span></span>
<span data-ttu-id="1323a-106">Il cmdlet **Start-AzureRmServiceBusMigration** crea una nuova configurazione di migrazione e avvia la migrazione delle entità da standard a spazi dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="1323a-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="1323a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1323a-107">EXAMPLES</span></span>

### <span data-ttu-id="1323a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1323a-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="1323a-109">Crea una nuova configurazione di migrazione per gli spazi dei nomi "TestingNamespaceStandardMirgation" in "TestingNamespacePremiumMirgation"</span><span class="sxs-lookup"><span data-stu-id="1323a-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="1323a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1323a-110">PARAMETERS</span></span>

### <span data-ttu-id="1323a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1323a-111">-AsJob</span></span>
<span data-ttu-id="1323a-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1323a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1323a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1323a-113">-DefaultProfile</span></span>
<span data-ttu-id="1323a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1323a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1323a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1323a-115">-Name</span></span>
<span data-ttu-id="1323a-116">Nome dello spazio dei nomi standard</span><span class="sxs-lookup"><span data-stu-id="1323a-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="1323a-117">-Postmigrationname</span><span class="sxs-lookup"><span data-stu-id="1323a-117">-PostMigrationName</span></span>
<span data-ttu-id="1323a-118">Pubblicare il nome della migrazione per lo spazio dei nomi standrad in migrazione</span><span class="sxs-lookup"><span data-stu-id="1323a-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="1323a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1323a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1323a-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1323a-120">Resource Group Name</span></span>

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

### <span data-ttu-id="1323a-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="1323a-121">-TargetNameSpace</span></span>
<span data-ttu-id="1323a-122">ID ARM dello spazio dei nomi Premium</span><span class="sxs-lookup"><span data-stu-id="1323a-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="1323a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1323a-123">-Confirm</span></span>
<span data-ttu-id="1323a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1323a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1323a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1323a-125">-WhatIf</span></span>
<span data-ttu-id="1323a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1323a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1323a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1323a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1323a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1323a-128">CommonParameters</span></span>
<span data-ttu-id="1323a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1323a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1323a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1323a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1323a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1323a-131">INPUTS</span></span>

### <span data-ttu-id="1323a-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1323a-132">None</span></span>

## <span data-ttu-id="1323a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1323a-133">OUTPUTS</span></span>

### <span data-ttu-id="1323a-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1323a-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="1323a-135">Note</span><span class="sxs-lookup"><span data-stu-id="1323a-135">NOTES</span></span>

## <span data-ttu-id="1323a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1323a-136">RELATED LINKS</span></span>
