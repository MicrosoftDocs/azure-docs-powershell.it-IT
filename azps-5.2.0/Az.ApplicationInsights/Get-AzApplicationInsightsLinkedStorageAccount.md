---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353548"
---
# <span data-ttu-id="a31ab-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a31ab-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a31ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a31ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a31ab-103">Ottenere l'account di archiviazione collegato dell'applicazione Insights</span><span class="sxs-lookup"><span data-stu-id="a31ab-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="a31ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a31ab-104">SYNTAX</span></span>

### <span data-ttu-id="a31ab-105">ByResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a31ab-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a31ab-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a31ab-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a31ab-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a31ab-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a31ab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a31ab-108">DESCRIPTION</span></span>
<span data-ttu-id="a31ab-109">Ottenere l'account di archiviazione collegato dell'applicazione Insights</span><span class="sxs-lookup"><span data-stu-id="a31ab-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="a31ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a31ab-110">EXAMPLES</span></span>

### <span data-ttu-id="a31ab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a31ab-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="a31ab-112">Ottenere l'account di archiviazione collegato associato al componente "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="a31ab-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="a31ab-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a31ab-113">PARAMETERS</span></span>

### <span data-ttu-id="a31ab-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a31ab-114">-ComponentName</span></span>
<span data-ttu-id="a31ab-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="a31ab-115">Component Name</span></span>

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

### <span data-ttu-id="a31ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31ab-116">-DefaultProfile</span></span>
<span data-ttu-id="a31ab-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a31ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a31ab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a31ab-118">-InputObject</span></span>
<span data-ttu-id="a31ab-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a31ab-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="a31ab-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a31ab-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a31ab-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a31ab-122">-ResourceId</span></span>
<span data-ttu-id="a31ab-123">Componente ResourceId</span><span class="sxs-lookup"><span data-stu-id="a31ab-123">Component ResourceId</span></span>

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

### <span data-ttu-id="a31ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31ab-124">CommonParameters</span></span>
<span data-ttu-id="a31ab-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31ab-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a31ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31ab-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a31ab-127">INPUTS</span></span>

### <span data-ttu-id="a31ab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a31ab-128">System.String</span></span>

### <span data-ttu-id="a31ab-129">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a31ab-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a31ab-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a31ab-130">OUTPUTS</span></span>

### <span data-ttu-id="a31ab-131">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a31ab-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="a31ab-132">Note</span><span class="sxs-lookup"><span data-stu-id="a31ab-132">NOTES</span></span>

## <span data-ttu-id="a31ab-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a31ab-133">RELATED LINKS</span></span>
