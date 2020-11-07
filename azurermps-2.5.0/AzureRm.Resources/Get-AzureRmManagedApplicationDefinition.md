---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: e6df93dee8599c6bae42cc9428b2a7691abf4740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866448"
---
# <span data-ttu-id="23997-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="23997-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="23997-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23997-102">SYNOPSIS</span></span>
<span data-ttu-id="23997-103">Ottiene le definizioni di applicazione gestite</span><span class="sxs-lookup"><span data-stu-id="23997-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23997-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23997-104">SYNTAX</span></span>

### <span data-ttu-id="23997-105">GetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23997-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23997-106">GetById</span><span class="sxs-lookup"><span data-stu-id="23997-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23997-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23997-107">DESCRIPTION</span></span>
<span data-ttu-id="23997-108">Il cmdlet **Get-AzureRmManagedApplicationDefinition** ottiene le definizioni di applicazione gestite</span><span class="sxs-lookup"><span data-stu-id="23997-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="23997-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23997-109">EXAMPLES</span></span>

### <span data-ttu-id="23997-110">Esempio 1: ottenere tutte le definizioni di applicazione gestite in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="23997-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="23997-111">Questo comando consente di ottenere le definizioni di applicazione gestite in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="23997-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="23997-112">Esempio 2: ottenere una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="23997-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="23997-113">Questo comando ottiene la definizione dell'applicazione gestita "myManagedAppDef" in gruppo risorse "MyRG"</span><span class="sxs-lookup"><span data-stu-id="23997-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="23997-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23997-114">PARAMETERS</span></span>

### <span data-ttu-id="23997-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23997-115">-ApiVersion</span></span>
<span data-ttu-id="23997-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="23997-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="23997-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="23997-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23997-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23997-118">-DefaultProfile</span></span>
<span data-ttu-id="23997-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23997-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23997-120">-ID</span><span class="sxs-lookup"><span data-stu-id="23997-120">-Id</span></span>
<span data-ttu-id="23997-121">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="23997-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="23997-122">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="23997-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23997-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="23997-123">-Name</span></span>
<span data-ttu-id="23997-124">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="23997-124">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23997-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="23997-125">-Pre</span></span>
<span data-ttu-id="23997-126">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="23997-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23997-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23997-127">-ResourceGroupName</span></span>
<span data-ttu-id="23997-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23997-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23997-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23997-129">CommonParameters</span></span>
<span data-ttu-id="23997-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23997-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23997-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23997-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23997-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23997-132">INPUTS</span></span>

### <span data-ttu-id="23997-133">System. String</span><span class="sxs-lookup"><span data-stu-id="23997-133">System.String</span></span>

## <span data-ttu-id="23997-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23997-134">OUTPUTS</span></span>

### <span data-ttu-id="23997-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="23997-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="23997-136">Note</span><span class="sxs-lookup"><span data-stu-id="23997-136">NOTES</span></span>

## <span data-ttu-id="23997-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23997-137">RELATED LINKS</span></span>
