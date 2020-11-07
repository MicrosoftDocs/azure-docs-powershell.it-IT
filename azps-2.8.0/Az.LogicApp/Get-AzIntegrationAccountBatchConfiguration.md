---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 5920ba51d4b067b7c47de6c471240a193efb3e5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674047"
---
# <span data-ttu-id="fe75d-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe75d-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="fe75d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe75d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe75d-103">Ottiene una configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe75d-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="fe75d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe75d-104">SYNTAX</span></span>

### <span data-ttu-id="fe75d-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe75d-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe75d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe75d-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe75d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe75d-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe75d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe75d-108">DESCRIPTION</span></span>
<span data-ttu-id="fe75d-109">Il cmdlet **Get-AzIntegrationAccountBatchConfiguration** ottiene una configurazione batch da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe75d-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="fe75d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe75d-110">EXAMPLES</span></span>

### <span data-ttu-id="fe75d-111">Esempio 1: ottenere una configurazione batch per parametri</span><span class="sxs-lookup"><span data-stu-id="fe75d-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fe75d-112">Ottenere una configurazione batch denominata "sampleBatchConfig" situata nell'account di integrazione "sampleIntegrationAccount", contenuta nel gruppo risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="fe75d-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="fe75d-113">Esempio 2: elencare tutte le configurazioni batch in un account di integrazione per parametri</span><span class="sxs-lookup"><span data-stu-id="fe75d-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fe75d-114">Ottenere tutte le configurazioni batch presenti nell'account di integrazione "sampleIntegrationAccount" contenuto nel gruppo di risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="fe75d-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="fe75d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe75d-115">PARAMETERS</span></span>

### <span data-ttu-id="fe75d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe75d-116">-DefaultProfile</span></span>
<span data-ttu-id="fe75d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe75d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe75d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe75d-118">-Name</span></span>
<span data-ttu-id="fe75d-119">Nome della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe75d-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe75d-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="fe75d-120">-ParentName</span></span>
<span data-ttu-id="fe75d-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe75d-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe75d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fe75d-122">-ParentObject</span></span>
<span data-ttu-id="fe75d-123">Un oggetto account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe75d-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe75d-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fe75d-124">-ParentResourceId</span></span>
<span data-ttu-id="fe75d-125">ID risorsa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe75d-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe75d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe75d-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe75d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe75d-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe75d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe75d-128">CommonParameters</span></span>
<span data-ttu-id="fe75d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe75d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe75d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe75d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe75d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe75d-131">INPUTS</span></span>

### <span data-ttu-id="fe75d-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fe75d-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="fe75d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fe75d-133">System.String</span></span>

## <span data-ttu-id="fe75d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe75d-134">OUTPUTS</span></span>

### <span data-ttu-id="fe75d-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe75d-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="fe75d-136">Note</span><span class="sxs-lookup"><span data-stu-id="fe75d-136">NOTES</span></span>

## <span data-ttu-id="fe75d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe75d-137">RELATED LINKS</span></span>
