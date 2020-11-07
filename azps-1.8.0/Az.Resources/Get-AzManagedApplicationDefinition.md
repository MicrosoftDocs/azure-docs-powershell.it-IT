---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: af8d117611eafbeaf79a107e0066ec60b58524e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677401"
---
# <span data-ttu-id="58af7-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="58af7-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="58af7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58af7-102">SYNOPSIS</span></span>
<span data-ttu-id="58af7-103">Ottiene le definizioni di applicazione gestite</span><span class="sxs-lookup"><span data-stu-id="58af7-103">Gets managed application definitions</span></span>

## <span data-ttu-id="58af7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58af7-104">SYNTAX</span></span>

### <span data-ttu-id="58af7-105">GetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58af7-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58af7-106">GetById</span><span class="sxs-lookup"><span data-stu-id="58af7-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58af7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58af7-107">DESCRIPTION</span></span>
<span data-ttu-id="58af7-108">Il cmdlet **Get-AzManagedApplicationDefinition** ottiene le definizioni di applicazione gestite</span><span class="sxs-lookup"><span data-stu-id="58af7-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="58af7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58af7-109">EXAMPLES</span></span>

### <span data-ttu-id="58af7-110">Esempio 1: ottenere tutte le definizioni di applicazione gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="58af7-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="58af7-111">Questo comando consente di ottenere le definizioni di applicazione gestite in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="58af7-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="58af7-112">Esempio 2: ottenere una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="58af7-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="58af7-113">Questo comando ottiene la definizione dell'applicazione gestita "myManagedAppDef" in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="58af7-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="58af7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58af7-114">PARAMETERS</span></span>

### <span data-ttu-id="58af7-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="58af7-115">-ApiVersion</span></span>
<span data-ttu-id="58af7-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="58af7-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="58af7-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="58af7-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58af7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58af7-118">-DefaultProfile</span></span>
<span data-ttu-id="58af7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58af7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58af7-120">-ID</span><span class="sxs-lookup"><span data-stu-id="58af7-120">-Id</span></span>
<span data-ttu-id="58af7-121">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="58af7-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="58af7-122">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="58af7-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58af7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="58af7-123">-Name</span></span>
<span data-ttu-id="58af7-124">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="58af7-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58af7-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="58af7-125">-Pre</span></span>
<span data-ttu-id="58af7-126">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="58af7-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="58af7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58af7-127">-ResourceGroupName</span></span>
<span data-ttu-id="58af7-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58af7-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58af7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58af7-129">CommonParameters</span></span>
<span data-ttu-id="58af7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58af7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58af7-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58af7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58af7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58af7-132">INPUTS</span></span>

### <span data-ttu-id="58af7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="58af7-133">System.String</span></span>

## <span data-ttu-id="58af7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58af7-134">OUTPUTS</span></span>

### <span data-ttu-id="58af7-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="58af7-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="58af7-136">Note</span><span class="sxs-lookup"><span data-stu-id="58af7-136">NOTES</span></span>

## <span data-ttu-id="58af7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58af7-137">RELATED LINKS</span></span>
