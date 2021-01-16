---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 2d1c4b2f272516af31fba17db50d33991dd1db50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476787"
---
# <span data-ttu-id="dfae2-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="dfae2-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="dfae2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfae2-102">SYNOPSIS</span></span>
<span data-ttu-id="dfae2-103">Ottenere o elencare la categoria di impostazioni di diagnostica supportate per la risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="dfae2-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="dfae2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfae2-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfae2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfae2-105">DESCRIPTION</span></span>
<span data-ttu-id="dfae2-106">Ottenere o elencare la categoria di impostazioni di diagnostica supportate per la risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="dfae2-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="dfae2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfae2-107">EXAMPLES</span></span>

### <span data-ttu-id="dfae2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dfae2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSetting -TargetResourceId -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="dfae2-109">Ottenere le categorie di impostazioni di diagnostica supportate per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfae2-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="dfae2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfae2-110">PARAMETERS</span></span>

### <span data-ttu-id="dfae2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfae2-111">-DefaultProfile</span></span>
<span data-ttu-id="dfae2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfae2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfae2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfae2-113">-Name</span></span>
<span data-ttu-id="dfae2-114">Nome della categoria dell'impostazione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="dfae2-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="dfae2-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dfae2-115">-TargetResourceId</span></span>
<span data-ttu-id="dfae2-116">ID risorsa di destinazione</span><span class="sxs-lookup"><span data-stu-id="dfae2-116">Target resource Id</span></span>

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

### <span data-ttu-id="dfae2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfae2-117">CommonParameters</span></span>
<span data-ttu-id="dfae2-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfae2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfae2-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfae2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfae2-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfae2-120">INPUTS</span></span>

### <span data-ttu-id="dfae2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="dfae2-121">System.String</span></span>

## <span data-ttu-id="dfae2-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfae2-122">OUTPUTS</span></span>

### <span data-ttu-id="dfae2-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="dfae2-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="dfae2-124">Note</span><span class="sxs-lookup"><span data-stu-id="dfae2-124">NOTES</span></span>

## <span data-ttu-id="dfae2-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfae2-125">RELATED LINKS</span></span>
