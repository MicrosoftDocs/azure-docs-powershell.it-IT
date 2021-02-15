---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197870"
---
# <span data-ttu-id="bcf9e-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="bcf9e-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="bcf9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf9e-103">Recupera MigrationConfiguration per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcf9e-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="bcf9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcf9e-104">SYNTAX</span></span>

### <span data-ttu-id="bcf9e-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcf9e-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcf9e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bcf9e-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf9e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf9e-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcf9e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bcf9e-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf9e-109">**Get-AzServiceBusMigration** Recupera la configurazione di migrazione per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcf9e-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="bcf9e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcf9e-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf9e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcf9e-111">Example 1</span></span>
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

<span data-ttu-id="bcf9e-112">Ottiene le proprietà di configurazione della migrazione di 'TestingStandardMigration'</span><span class="sxs-lookup"><span data-stu-id="bcf9e-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="bcf9e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcf9e-113">PARAMETERS</span></span>

### <span data-ttu-id="bcf9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf9e-114">-DefaultProfile</span></span>
<span data-ttu-id="bcf9e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf9e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf9e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcf9e-116">-InputObject</span></span>
<span data-ttu-id="bcf9e-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="bcf9e-117">Namespace Object</span></span>

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

### <span data-ttu-id="bcf9e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bcf9e-118">-Name</span></span>
<span data-ttu-id="bcf9e-119">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcf9e-119">Namespace Name</span></span>

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

### <span data-ttu-id="bcf9e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf9e-120">-ResourceGroupName</span></span>
<span data-ttu-id="bcf9e-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bcf9e-121">Resource Group Name</span></span>

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

### <span data-ttu-id="bcf9e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf9e-122">-ResourceId</span></span>
<span data-ttu-id="bcf9e-123">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcf9e-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="bcf9e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf9e-124">CommonParameters</span></span>
<span data-ttu-id="bcf9e-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf9e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf9e-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf9e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf9e-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="bcf9e-127">INPUTS</span></span>

### <span data-ttu-id="bcf9e-128">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="bcf9e-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="bcf9e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bcf9e-129">System.String</span></span>

## <span data-ttu-id="bcf9e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcf9e-130">OUTPUTS</span></span>

### <span data-ttu-id="bcf9e-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bcf9e-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="bcf9e-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="bcf9e-132">NOTES</span></span>

## <span data-ttu-id="bcf9e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcf9e-133">RELATED LINKS</span></span>
