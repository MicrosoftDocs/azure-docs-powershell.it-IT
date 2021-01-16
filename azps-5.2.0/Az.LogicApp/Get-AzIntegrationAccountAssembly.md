---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344572"
---
# <span data-ttu-id="d0dd2-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d0dd2-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d0dd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="d0dd2-103">Ottiene un assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="d0dd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0dd2-104">SYNTAX</span></span>

### <span data-ttu-id="d0dd2-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0dd2-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0dd2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0dd2-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0dd2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0dd2-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0dd2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0dd2-108">DESCRIPTION</span></span>
<span data-ttu-id="d0dd2-109">Il cmdlet **Get-AzIntegrationAccountAssembly** ottiene un assembly da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="d0dd2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0dd2-110">EXAMPLES</span></span>

### <span data-ttu-id="d0dd2-111">Esempio 1: ottenere un assembly in base a parametri</span><span class="sxs-lookup"><span data-stu-id="d0dd2-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d0dd2-112">Ottenere un assembly denominato "sampleAssembly" situato nell'account di integrazione "sampleIntegrationAccount" contenuto nel gruppo di risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d0dd2-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="d0dd2-113">Esempio 2: elencare tutti gli assembly in un account di integrazione per parametri</span><span class="sxs-lookup"><span data-stu-id="d0dd2-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d0dd2-114">Ottenere tutti gli assembly presenti nell'account di integrazione "sampleIntegrationAccount" contenuto nel gruppo di risorse "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="d0dd2-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="d0dd2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0dd2-115">PARAMETERS</span></span>

### <span data-ttu-id="d0dd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0dd2-116">-DefaultProfile</span></span>
<span data-ttu-id="d0dd2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0dd2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0dd2-118">-Name</span></span>
<span data-ttu-id="d0dd2-119">Nome dell'assembly dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd2-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d0dd2-120">-ParentName</span></span>
<span data-ttu-id="d0dd2-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-121">The integration account name.</span></span>

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

### <span data-ttu-id="d0dd2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0dd2-122">-ParentObject</span></span>
<span data-ttu-id="d0dd2-123">Un oggetto account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-123">An integration account object.</span></span>

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

### <span data-ttu-id="d0dd2-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0dd2-124">-ParentResourceId</span></span>
<span data-ttu-id="d0dd2-125">ID risorsa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="d0dd2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0dd2-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0dd2-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-127">The resource group name.</span></span>

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

### <span data-ttu-id="d0dd2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0dd2-128">CommonParameters</span></span>
<span data-ttu-id="d0dd2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0dd2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0dd2-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0dd2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0dd2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0dd2-131">INPUTS</span></span>

### <span data-ttu-id="d0dd2-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d0dd2-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d0dd2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d0dd2-133">System.String</span></span>

## <span data-ttu-id="d0dd2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0dd2-134">OUTPUTS</span></span>

### <span data-ttu-id="d0dd2-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d0dd2-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d0dd2-136">Note</span><span class="sxs-lookup"><span data-stu-id="d0dd2-136">NOTES</span></span>

## <span data-ttu-id="d0dd2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0dd2-137">RELATED LINKS</span></span>
