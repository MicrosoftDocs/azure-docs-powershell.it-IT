---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: b78836a7d122dc05e4cd621b2d8994bd55697687
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677163"
---
# <span data-ttu-id="308fb-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="308fb-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="308fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="308fb-102">SYNOPSIS</span></span>
<span data-ttu-id="308fb-103">Recupera MigrationConfiguration per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="308fb-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="308fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="308fb-104">SYNTAX</span></span>

### <span data-ttu-id="308fb-105">MigrationConfigurationPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="308fb-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="308fb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="308fb-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="308fb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="308fb-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="308fb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="308fb-108">DESCRIPTION</span></span>
<span data-ttu-id="308fb-109">**Get-AzServiceBusMigration** recupera la configurazione di migrazione per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="308fb-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="308fb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="308fb-110">EXAMPLES</span></span>

### <span data-ttu-id="308fb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="308fb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="308fb-112">Ottiene le proprietà di configurazione della migrazione di "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="308fb-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="308fb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="308fb-113">PARAMETERS</span></span>

### <span data-ttu-id="308fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308fb-114">-DefaultProfile</span></span>
<span data-ttu-id="308fb-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="308fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="308fb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="308fb-116">-InputObject</span></span>
<span data-ttu-id="308fb-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="308fb-117">Namespace Object</span></span>

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

### <span data-ttu-id="308fb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="308fb-118">-Name</span></span>
<span data-ttu-id="308fb-119">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="308fb-119">Namespace Name</span></span>

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

### <span data-ttu-id="308fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="308fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="308fb-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="308fb-121">Resource Group Name</span></span>

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

### <span data-ttu-id="308fb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="308fb-122">-ResourceId</span></span>
<span data-ttu-id="308fb-123">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="308fb-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="308fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308fb-124">CommonParameters</span></span>
<span data-ttu-id="308fb-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308fb-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308fb-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="308fb-127">INPUTS</span></span>

### <span data-ttu-id="308fb-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="308fb-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="308fb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="308fb-129">System.String</span></span>

## <span data-ttu-id="308fb-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="308fb-130">OUTPUTS</span></span>

### <span data-ttu-id="308fb-131">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="308fb-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="308fb-132">Note</span><span class="sxs-lookup"><span data-stu-id="308fb-132">NOTES</span></span>

## <span data-ttu-id="308fb-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="308fb-133">RELATED LINKS</span></span>
