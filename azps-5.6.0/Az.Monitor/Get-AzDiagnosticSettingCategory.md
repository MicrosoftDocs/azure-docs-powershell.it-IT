---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: df263698a913faf361e5f23bb12d0267be314106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980061"
---
# <span data-ttu-id="8b4f4-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="8b4f4-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="8b4f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4f4-103">Ottenere o elencare la categoria di impostazioni diagnostiche supportate per la risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4f4-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="8b4f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b4f4-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b4f4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="8b4f4-106">Ottenere o elencare la categoria di impostazioni diagnostiche supportate per la risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4f4-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="8b4f4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b4f4-107">EXAMPLES</span></span>

### <span data-ttu-id="8b4f4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b4f4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="8b4f4-109">Ottieni le categorie di impostazioni diagnostiche supportate per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b4f4-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="8b4f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b4f4-110">PARAMETERS</span></span>

### <span data-ttu-id="8b4f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4f4-111">-DefaultProfile</span></span>
<span data-ttu-id="8b4f4-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b4f4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8b4f4-113">-Name</span></span>
<span data-ttu-id="8b4f4-114">Nome della categoria delle impostazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="8b4f4-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="8b4f4-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8b4f4-115">-TargetResourceId</span></span>
<span data-ttu-id="8b4f4-116">ID risorsa di destinazione</span><span class="sxs-lookup"><span data-stu-id="8b4f4-116">Target resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4f4-117">CommonParameters</span></span>
<span data-ttu-id="8b4f4-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4f4-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b4f4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4f4-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b4f4-120">INPUTS</span></span>

### <span data-ttu-id="8b4f4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8b4f4-121">System.String</span></span>

## <span data-ttu-id="8b4f4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b4f4-122">OUTPUTS</span></span>

### <span data-ttu-id="8b4f4-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="8b4f4-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="8b4f4-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b4f4-124">NOTES</span></span>

## <span data-ttu-id="8b4f4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b4f4-125">RELATED LINKS</span></span>
