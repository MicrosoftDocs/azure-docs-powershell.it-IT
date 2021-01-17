---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332563"
---
# <span data-ttu-id="b3a81-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b3a81-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="b3a81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3a81-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a81-103">Elenco configurationAssignments per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3a81-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b3a81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3a81-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3a81-105">DESCRIPTION</span></span>
<span data-ttu-id="b3a81-106">Elenco configurationAssignments per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3a81-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b3a81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3a81-107">EXAMPLES</span></span>

### <span data-ttu-id="b3a81-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3a81-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="b3a81-109">Elenco configurationAssignments per host dedicato.</span><span class="sxs-lookup"><span data-stu-id="b3a81-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="b3a81-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3a81-110">PARAMETERS</span></span>

### <span data-ttu-id="b3a81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a81-111">-DefaultProfile</span></span>
<span data-ttu-id="b3a81-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a81-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a81-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="b3a81-113">-ProviderName</span></span>
<span data-ttu-id="b3a81-114">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3a81-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a81-115">-ResourceGroupName</span></span>
<span data-ttu-id="b3a81-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3a81-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a81-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b3a81-117">-ResourceName</span></span>
<span data-ttu-id="b3a81-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3a81-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a81-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="b3a81-119">-ResourceParentName</span></span>
<span data-ttu-id="b3a81-120">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="b3a81-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a81-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="b3a81-121">-ResourceParentType</span></span>
<span data-ttu-id="b3a81-122">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="b3a81-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a81-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b3a81-123">-ResourceType</span></span>
<span data-ttu-id="b3a81-124">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3a81-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a81-125">CommonParameters</span></span>
<span data-ttu-id="b3a81-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a81-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3a81-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a81-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3a81-128">INPUTS</span></span>

### <span data-ttu-id="b3a81-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a81-129">System.String</span></span>

## <span data-ttu-id="b3a81-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3a81-130">OUTPUTS</span></span>

### <span data-ttu-id="b3a81-131">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b3a81-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="b3a81-132">Note</span><span class="sxs-lookup"><span data-stu-id="b3a81-132">NOTES</span></span>

## <span data-ttu-id="b3a81-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3a81-133">RELATED LINKS</span></span>
