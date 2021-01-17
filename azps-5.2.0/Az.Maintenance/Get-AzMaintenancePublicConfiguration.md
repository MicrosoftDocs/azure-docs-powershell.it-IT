---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340864"
---
# <span data-ttu-id="3d8ed-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d8ed-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="3d8ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8ed-103">Ottenere il record di configurazione della manutenzione pubblica</span><span class="sxs-lookup"><span data-stu-id="3d8ed-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="3d8ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d8ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="3d8ed-106">Ottenere il record di configurazione della manutenzione pubblica</span><span class="sxs-lookup"><span data-stu-id="3d8ed-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="3d8ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="3d8ed-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d8ed-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="3d8ed-109">Ottenere il record di configurazione della manutenzione pubblica</span><span class="sxs-lookup"><span data-stu-id="3d8ed-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="3d8ed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-110">PARAMETERS</span></span>

### <span data-ttu-id="3d8ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8ed-111">-DefaultProfile</span></span>
<span data-ttu-id="3d8ed-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8ed-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d8ed-113">-Name</span></span>
<span data-ttu-id="3d8ed-114">Nome della configurazione della manutenzione pubblica.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8ed-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8ed-115">-ResourceGroupName</span></span>
<span data-ttu-id="3d8ed-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8ed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8ed-117">CommonParameters</span></span>
<span data-ttu-id="3d8ed-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8ed-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d8ed-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8ed-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-120">INPUTS</span></span>

### <span data-ttu-id="3d8ed-121">System. String</span><span class="sxs-lookup"><span data-stu-id="3d8ed-121">System.String</span></span>

## <span data-ttu-id="3d8ed-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d8ed-122">OUTPUTS</span></span>

### <span data-ttu-id="3d8ed-123">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d8ed-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="3d8ed-124">Note</span><span class="sxs-lookup"><span data-stu-id="3d8ed-124">NOTES</span></span>

## <span data-ttu-id="3d8ed-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-125">RELATED LINKS</span></span>
