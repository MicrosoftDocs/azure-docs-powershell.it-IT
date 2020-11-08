---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021709"
---
# <span data-ttu-id="bd8a9-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="bd8a9-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="bd8a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8a9-103">Recupera MigrationConfiguration per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd8a9-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="bd8a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd8a9-104">SYNTAX</span></span>

### <span data-ttu-id="bd8a9-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd8a9-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd8a9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd8a9-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd8a9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd8a9-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd8a9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd8a9-108">DESCRIPTION</span></span>
<span data-ttu-id="bd8a9-109">**Get-AzServiceBusMigration** recupera la configurazione di migrazione per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd8a9-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="bd8a9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd8a9-110">EXAMPLES</span></span>

### <span data-ttu-id="bd8a9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd8a9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="bd8a9-112">Ottiene le proprietà di configurazione della migrazione di "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="bd8a9-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="bd8a9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd8a9-113">PARAMETERS</span></span>

### <span data-ttu-id="bd8a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8a9-114">-DefaultProfile</span></span>
<span data-ttu-id="bd8a9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd8a9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd8a9-116">-InputObject</span></span>
<span data-ttu-id="bd8a9-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="bd8a9-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8a9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd8a9-118">-Name</span></span>
<span data-ttu-id="bd8a9-119">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd8a9-119">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8a9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd8a9-120">-ResourceGroupName</span></span>
<span data-ttu-id="bd8a9-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bd8a9-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8a9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd8a9-122">-ResourceId</span></span>
<span data-ttu-id="bd8a9-123">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd8a9-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8a9-124">CommonParameters</span></span>
<span data-ttu-id="bd8a9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd8a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8a9-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd8a9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8a9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd8a9-127">INPUTS</span></span>

### <span data-ttu-id="bd8a9-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bd8a9-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="bd8a9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bd8a9-129">System.String</span></span>

## <span data-ttu-id="bd8a9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd8a9-130">OUTPUTS</span></span>

### <span data-ttu-id="bd8a9-131">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bd8a9-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="bd8a9-132">Note</span><span class="sxs-lookup"><span data-stu-id="bd8a9-132">NOTES</span></span>

## <span data-ttu-id="bd8a9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd8a9-133">RELATED LINKS</span></span>
