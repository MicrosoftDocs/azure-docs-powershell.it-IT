---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203748"
---
# <span data-ttu-id="4d442-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d442-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="4d442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d442-102">SYNOPSIS</span></span>
<span data-ttu-id="4d442-103">Recupera una configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d442-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="4d442-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d442-104">SYNTAX</span></span>

### <span data-ttu-id="4d442-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d442-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d442-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d442-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d442-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d442-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d442-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d442-108">DESCRIPTION</span></span>
<span data-ttu-id="4d442-109">Il cmdlet **Get-AzIntegrationAccountBatchConfiguration** ottiene una configurazione batch da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d442-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="4d442-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d442-110">EXAMPLES</span></span>

### <span data-ttu-id="4d442-111">Esempio 1: Ottenere una configurazione batch per parametri</span><span class="sxs-lookup"><span data-stu-id="4d442-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="4d442-112">Ottenere una configurazione batch denominata "sampleBatchConfig" che si trova nell'account di integrazione "sampleIntegrationAccount" contenuto nel gruppo di risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="4d442-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="4d442-113">Esempio 2: Elencare tutte le configurazioni di batch in un account di integrazione in base ai parametri</span><span class="sxs-lookup"><span data-stu-id="4d442-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="4d442-114">Ottenere tutte le configurazioni batch nell'account di integrazione "sampleIntegrationAccount" contenuto nel gruppo di risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="4d442-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="4d442-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d442-115">PARAMETERS</span></span>

### <span data-ttu-id="4d442-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d442-116">-DefaultProfile</span></span>
<span data-ttu-id="4d442-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d442-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d442-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4d442-118">-Name</span></span>
<span data-ttu-id="4d442-119">Nome di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d442-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="4d442-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="4d442-120">-ParentName</span></span>
<span data-ttu-id="4d442-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d442-121">The integration account name.</span></span>

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

### <span data-ttu-id="4d442-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d442-122">-ParentObject</span></span>
<span data-ttu-id="4d442-123">Oggetto account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d442-123">An integration account object.</span></span>

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

### <span data-ttu-id="4d442-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4d442-124">-ParentResourceId</span></span>
<span data-ttu-id="4d442-125">ID risorsa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4d442-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="4d442-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d442-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d442-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d442-127">The resource group name.</span></span>

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

### <span data-ttu-id="4d442-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d442-128">CommonParameters</span></span>
<span data-ttu-id="4d442-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d442-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d442-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d442-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d442-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d442-131">INPUTS</span></span>

### <span data-ttu-id="4d442-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4d442-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="4d442-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d442-133">System.String</span></span>

## <span data-ttu-id="4d442-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d442-134">OUTPUTS</span></span>

### <span data-ttu-id="4d442-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d442-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="4d442-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d442-136">NOTES</span></span>

## <span data-ttu-id="4d442-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d442-137">RELATED LINKS</span></span>
