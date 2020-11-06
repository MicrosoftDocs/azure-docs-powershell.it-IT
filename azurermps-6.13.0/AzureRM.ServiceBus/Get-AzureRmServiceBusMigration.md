---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516488"
---
# <span data-ttu-id="426a6-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="426a6-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="426a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="426a6-102">SYNOPSIS</span></span>
<span data-ttu-id="426a6-103">Recupera MigrationConfiguration per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="426a6-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="426a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="426a6-104">SYNTAX</span></span>

### <span data-ttu-id="426a6-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="426a6-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="426a6-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="426a6-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="426a6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="426a6-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="426a6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="426a6-108">DESCRIPTION</span></span>
<span data-ttu-id="426a6-109">**Get-AzureRmServiceBusMigration** recupera la configurazione di migrazione per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="426a6-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="426a6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="426a6-110">EXAMPLES</span></span>

### <span data-ttu-id="426a6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="426a6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="426a6-112">Ottiene le proprietà di configurazione della migrazione di "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="426a6-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="426a6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="426a6-113">PARAMETERS</span></span>

### <span data-ttu-id="426a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426a6-114">-DefaultProfile</span></span>
<span data-ttu-id="426a6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="426a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="426a6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="426a6-116">-InputObject</span></span>
<span data-ttu-id="426a6-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="426a6-117">Namespace Object</span></span>

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

### <span data-ttu-id="426a6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="426a6-118">-Name</span></span>
<span data-ttu-id="426a6-119">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="426a6-119">Namespace Name</span></span>

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

### <span data-ttu-id="426a6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426a6-120">-ResourceGroupName</span></span>
<span data-ttu-id="426a6-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="426a6-121">Resource Group Name</span></span>

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

### <span data-ttu-id="426a6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="426a6-122">-ResourceId</span></span>
<span data-ttu-id="426a6-123">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="426a6-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="426a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426a6-124">CommonParameters</span></span>
<span data-ttu-id="426a6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426a6-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426a6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426a6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="426a6-127">INPUTS</span></span>

### <span data-ttu-id="426a6-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="426a6-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="426a6-129">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="426a6-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="426a6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="426a6-130">System.String</span></span>

## <span data-ttu-id="426a6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="426a6-131">OUTPUTS</span></span>

### <span data-ttu-id="426a6-132">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="426a6-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="426a6-133">Note</span><span class="sxs-lookup"><span data-stu-id="426a6-133">NOTES</span></span>

## <span data-ttu-id="426a6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="426a6-134">RELATED LINKS</span></span>
