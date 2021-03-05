---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: 6939cde26695cb4273d776437c3697c03d426db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984603"
---
# <span data-ttu-id="07b75-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="07b75-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="07b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b75-102">SYNOPSIS</span></span>
<span data-ttu-id="07b75-103">Record di configurazione Ottieni manutenzione</span><span class="sxs-lookup"><span data-stu-id="07b75-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="07b75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07b75-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07b75-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="07b75-105">DESCRIPTION</span></span>
<span data-ttu-id="07b75-106">Record di configurazione Ottieni manutenzione</span><span class="sxs-lookup"><span data-stu-id="07b75-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="07b75-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07b75-107">EXAMPLES</span></span>

### <span data-ttu-id="07b75-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07b75-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="07b75-109">Record di configurazione Ottieni manutenzione</span><span class="sxs-lookup"><span data-stu-id="07b75-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="07b75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07b75-110">PARAMETERS</span></span>

### <span data-ttu-id="07b75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b75-111">-DefaultProfile</span></span>
<span data-ttu-id="07b75-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07b75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b75-113">-Name</span><span class="sxs-lookup"><span data-stu-id="07b75-113">-Name</span></span>
<span data-ttu-id="07b75-114">Nome della configurazione di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="07b75-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07b75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b75-115">-ResourceGroupName</span></span>
<span data-ttu-id="07b75-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07b75-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07b75-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b75-117">CommonParameters</span></span>
<span data-ttu-id="07b75-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07b75-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b75-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="07b75-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b75-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="07b75-120">INPUTS</span></span>

### <span data-ttu-id="07b75-121">System.String</span><span class="sxs-lookup"><span data-stu-id="07b75-121">System.String</span></span>

## <span data-ttu-id="07b75-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07b75-122">OUTPUTS</span></span>

### <span data-ttu-id="07b75-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="07b75-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="07b75-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="07b75-124">NOTES</span></span>

## <span data-ttu-id="07b75-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07b75-125">RELATED LINKS</span></span>
