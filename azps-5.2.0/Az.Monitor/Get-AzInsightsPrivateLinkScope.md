---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367636"
---
# <span data-ttu-id="cc1ad-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cc1ad-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="cc1ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1ad-103">Ottenere l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="cc1ad-103">Get private link scope</span></span>

## <span data-ttu-id="cc1ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc1ad-104">SYNTAX</span></span>

### <span data-ttu-id="cc1ad-105">ByResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc1ad-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc1ad-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc1ad-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc1ad-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc1ad-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc1ad-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc1ad-108">DESCRIPTION</span></span>
<span data-ttu-id="cc1ad-109">Elenco o ottenere un ambito di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="cc1ad-109">List or get private link scope</span></span> 

## <span data-ttu-id="cc1ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc1ad-110">EXAMPLES</span></span>

### <span data-ttu-id="cc1ad-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cc1ad-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="cc1ad-112">Ambiti di collegamento elenco privato in gruppo risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="cc1ad-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="cc1ad-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cc1ad-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="cc1ad-114">Ottenere l'ambito dei collegamenti privati con il nome "scope_name" in gruppo risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="cc1ad-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="cc1ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc1ad-115">PARAMETERS</span></span>

### <span data-ttu-id="cc1ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1ad-116">-DefaultProfile</span></span>
<span data-ttu-id="cc1ad-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc1ad-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc1ad-118">-Name</span></span>
<span data-ttu-id="cc1ad-119">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="cc1ad-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="cc1ad-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cc1ad-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1ad-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc1ad-122">-ResourceId</span></span>
<span data-ttu-id="cc1ad-123">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="cc1ad-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1ad-124">CommonParameters</span></span>
<span data-ttu-id="cc1ad-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc1ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1ad-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc1ad-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1ad-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc1ad-127">INPUTS</span></span>

### <span data-ttu-id="cc1ad-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cc1ad-128">System.String</span></span>

## <span data-ttu-id="cc1ad-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc1ad-129">OUTPUTS</span></span>

### <span data-ttu-id="cc1ad-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cc1ad-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="cc1ad-131">Note</span><span class="sxs-lookup"><span data-stu-id="cc1ad-131">NOTES</span></span>

## <span data-ttu-id="cc1ad-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc1ad-132">RELATED LINKS</span></span>
