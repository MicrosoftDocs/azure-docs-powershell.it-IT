---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 29c65ef5f5ec3b2b54fb883da706ddc9a38e1d4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180175"
---
# <span data-ttu-id="aacaf-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="aacaf-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="aacaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aacaf-102">SYNOPSIS</span></span>
<span data-ttu-id="aacaf-103">Ottenere o elencare la categoria di impostazioni diagnostiche supportate per la risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="aacaf-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="aacaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aacaf-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aacaf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aacaf-105">DESCRIPTION</span></span>
<span data-ttu-id="aacaf-106">Ottenere o elencare la categoria di impostazioni diagnostiche supportate per la risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="aacaf-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="aacaf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aacaf-107">EXAMPLES</span></span>

### <span data-ttu-id="aacaf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aacaf-108">Example 1</span></span>
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

<span data-ttu-id="aacaf-109">Ottieni le categorie di impostazioni diagnostiche supportate per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="aacaf-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="aacaf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aacaf-110">PARAMETERS</span></span>

### <span data-ttu-id="aacaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacaf-111">-DefaultProfile</span></span>
<span data-ttu-id="aacaf-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aacaf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aacaf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="aacaf-113">-Name</span></span>
<span data-ttu-id="aacaf-114">Nome della categoria di impostazioni diagnostiche</span><span class="sxs-lookup"><span data-stu-id="aacaf-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="aacaf-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="aacaf-115">-TargetResourceId</span></span>
<span data-ttu-id="aacaf-116">ID risorsa di destinazione</span><span class="sxs-lookup"><span data-stu-id="aacaf-116">Target resource Id</span></span>

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

### <span data-ttu-id="aacaf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacaf-117">CommonParameters</span></span>
<span data-ttu-id="aacaf-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aacaf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacaf-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aacaf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacaf-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="aacaf-120">INPUTS</span></span>

### <span data-ttu-id="aacaf-121">System.String</span><span class="sxs-lookup"><span data-stu-id="aacaf-121">System.String</span></span>

## <span data-ttu-id="aacaf-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aacaf-122">OUTPUTS</span></span>

### <span data-ttu-id="aacaf-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="aacaf-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="aacaf-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="aacaf-124">NOTES</span></span>

## <span data-ttu-id="aacaf-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aacaf-125">RELATED LINKS</span></span>
