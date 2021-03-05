---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 722f2bd79230de11c12ab0448fb39ed3ad49f00d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960702"
---
# <span data-ttu-id="d7bed-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7bed-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="d7bed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7bed-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bed-103">Recupera una configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d7bed-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="d7bed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7bed-104">SYNTAX</span></span>

### <span data-ttu-id="d7bed-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7bed-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bed-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7bed-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bed-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bed-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7bed-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7bed-108">DESCRIPTION</span></span>
<span data-ttu-id="d7bed-109">Il cmdlet **Get-AzIntegrationAccountBatchConfiguration** ottiene una configurazione batch da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d7bed-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="d7bed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7bed-110">EXAMPLES</span></span>

### <span data-ttu-id="d7bed-111">Esempio 1: Ottenere una configurazione batch in base ai parametri</span><span class="sxs-lookup"><span data-stu-id="d7bed-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="d7bed-112">Ottenere una configurazione batch denominata "sampleBatchConfig" che si trova nell'account di integrazione "sampleIntegrationAccount" contenuto nel gruppo di risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d7bed-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="d7bed-113">Esempio 2: Elencare tutte le configurazioni di batch in un account di integrazione in base ai parametri</span><span class="sxs-lookup"><span data-stu-id="d7bed-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="d7bed-114">Ottenere tutte le configurazioni batch nell'account di integrazione "sampleIntegrationAccount" contenuto nel gruppo di risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d7bed-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="d7bed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7bed-115">PARAMETERS</span></span>

### <span data-ttu-id="d7bed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bed-116">-DefaultProfile</span></span>
<span data-ttu-id="d7bed-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7bed-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d7bed-118">-Name</span></span>
<span data-ttu-id="d7bed-119">Nome di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d7bed-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="d7bed-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d7bed-120">-ParentName</span></span>
<span data-ttu-id="d7bed-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d7bed-121">The integration account name.</span></span>

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

### <span data-ttu-id="d7bed-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7bed-122">-ParentObject</span></span>
<span data-ttu-id="d7bed-123">Oggetto account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d7bed-123">An integration account object.</span></span>

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

### <span data-ttu-id="d7bed-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bed-124">-ParentResourceId</span></span>
<span data-ttu-id="d7bed-125">ID risorsa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d7bed-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="d7bed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bed-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7bed-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d7bed-127">The resource group name.</span></span>

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

### <span data-ttu-id="d7bed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bed-128">CommonParameters</span></span>
<span data-ttu-id="d7bed-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7bed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bed-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bed-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bed-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7bed-131">INPUTS</span></span>

### <span data-ttu-id="d7bed-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d7bed-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d7bed-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d7bed-133">System.String</span></span>

## <span data-ttu-id="d7bed-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7bed-134">OUTPUTS</span></span>

### <span data-ttu-id="d7bed-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7bed-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="d7bed-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7bed-136">NOTES</span></span>

## <span data-ttu-id="d7bed-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7bed-137">RELATED LINKS</span></span>
