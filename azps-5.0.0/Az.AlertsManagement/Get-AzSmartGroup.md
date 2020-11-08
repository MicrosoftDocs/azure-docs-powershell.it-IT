---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199749"
---
# <span data-ttu-id="2c6c0-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="2c6c0-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="2c6c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6c0-103">Ottiene le informazioni sui gruppi smart</span><span class="sxs-lookup"><span data-stu-id="2c6c0-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="2c6c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c6c0-104">SYNTAX</span></span>

### <span data-ttu-id="2c6c0-105">SmartGroupsListByFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c6c0-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6c0-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="2c6c0-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c6c0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c6c0-107">DESCRIPTION</span></span>
<span data-ttu-id="2c6c0-108">Il cmdlet **Get-AzSmartGroup** ottiene le informazioni sui gruppi smart.</span><span class="sxs-lookup"><span data-stu-id="2c6c0-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="2c6c0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c6c0-109">EXAMPLES</span></span>

### <span data-ttu-id="2c6c0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2c6c0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="2c6c0-111">Elenca tutti i gruppi di Smart formati nell'ultima ora.</span><span class="sxs-lookup"><span data-stu-id="2c6c0-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="2c6c0-112">Usare Format-List per ottenere i dettagli completi di ogni gruppo di Smart in elenco.</span><span class="sxs-lookup"><span data-stu-id="2c6c0-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="2c6c0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2c6c0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="2c6c0-114">Ottenere i dettagli del gruppo smart per ID (GUID) o ID risorsa (ID ARM completo)</span><span class="sxs-lookup"><span data-stu-id="2c6c0-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="2c6c0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c6c0-115">PARAMETERS</span></span>

### <span data-ttu-id="2c6c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6c0-116">-DefaultProfile</span></span>
<span data-ttu-id="2c6c0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c6c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c6c0-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="2c6c0-118">-SmartGroupId</span></span>
<span data-ttu-id="2c6c0-119">Identificatore univoco di SmartGroup/ResourceId di SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="2c6c0-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6c0-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="2c6c0-120">-SortBy</span></span>
<span data-ttu-id="2c6c0-121">Proprietà Alert da usare durante l'ordinamento</span><span class="sxs-lookup"><span data-stu-id="2c6c0-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6c0-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="2c6c0-122">-SortOrder</span></span>
<span data-ttu-id="2c6c0-123">Ordine di ordinamento</span><span class="sxs-lookup"><span data-stu-id="2c6c0-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6c0-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="2c6c0-124">-TimeRange</span></span>
<span data-ttu-id="2c6c0-125">Valori di intervallo di tempo supportati-1h, 1D, 7D, 30D (il valore predefinito è 1D)</span><span class="sxs-lookup"><span data-stu-id="2c6c0-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6c0-126">CommonParameters</span></span>
<span data-ttu-id="2c6c0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c6c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6c0-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c6c0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6c0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c6c0-129">INPUTS</span></span>

### <span data-ttu-id="2c6c0-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2c6c0-130">None</span></span>

## <span data-ttu-id="2c6c0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c6c0-131">OUTPUTS</span></span>

### <span data-ttu-id="2c6c0-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="2c6c0-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="2c6c0-133">Note</span><span class="sxs-lookup"><span data-stu-id="2c6c0-133">NOTES</span></span>

## <span data-ttu-id="2c6c0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c6c0-134">RELATED LINKS</span></span>
