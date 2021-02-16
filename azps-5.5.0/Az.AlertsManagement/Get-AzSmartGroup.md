---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199798"
---
# <span data-ttu-id="f27e8-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="f27e8-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="f27e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f27e8-102">SYNOPSIS</span></span>
<span data-ttu-id="f27e8-103">Recupera informazioni sui gruppi intelligenti</span><span class="sxs-lookup"><span data-stu-id="f27e8-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="f27e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f27e8-104">SYNTAX</span></span>

### <span data-ttu-id="f27e8-105">SmartGroupsListByFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f27e8-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27e8-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="f27e8-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f27e8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f27e8-107">DESCRIPTION</span></span>
<span data-ttu-id="f27e8-108">Il cmdlet **Get-AzSmartGroup** ottiene informazioni sui gruppi intelligenti.</span><span class="sxs-lookup"><span data-stu-id="f27e8-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="f27e8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f27e8-109">EXAMPLES</span></span>

### <span data-ttu-id="f27e8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f27e8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="f27e8-111">Elencare tutti i gruppi intelligenti formati nell'ultima ora.</span><span class="sxs-lookup"><span data-stu-id="f27e8-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="f27e8-112">Usare Format-List per ottenere i dettagli completi di ogni gruppo intelligente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="f27e8-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="f27e8-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f27e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="f27e8-114">Ottenere i dettagli di un gruppo intelligente in base all'ID (GUID) o all'ID risorsa (ID ARM risorsa)</span><span class="sxs-lookup"><span data-stu-id="f27e8-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="f27e8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f27e8-115">PARAMETERS</span></span>

### <span data-ttu-id="f27e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27e8-116">-DefaultProfile</span></span>
<span data-ttu-id="f27e8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f27e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f27e8-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="f27e8-118">-SmartGroupId</span></span>
<span data-ttu-id="f27e8-119">Identificatore univoco di SmartGroup/ResourceId di SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="f27e8-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="f27e8-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="f27e8-120">-SortBy</span></span>
<span data-ttu-id="f27e8-121">Proprietà di avviso da usare durante l'ordinamento</span><span class="sxs-lookup"><span data-stu-id="f27e8-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="f27e8-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="f27e8-122">-SortOrder</span></span>
<span data-ttu-id="f27e8-123">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="f27e8-123">Sort Order</span></span>

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

### <span data-ttu-id="f27e8-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="f27e8-124">-TimeRange</span></span>
<span data-ttu-id="f27e8-125">Valori di intervallo di tempo supportati: 1h, 1d, 7d, 30d (il valore predefinito è 1d)</span><span class="sxs-lookup"><span data-stu-id="f27e8-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="f27e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27e8-126">CommonParameters</span></span>
<span data-ttu-id="f27e8-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27e8-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f27e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27e8-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="f27e8-129">INPUTS</span></span>

### <span data-ttu-id="f27e8-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f27e8-130">None</span></span>

## <span data-ttu-id="f27e8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f27e8-131">OUTPUTS</span></span>

### <span data-ttu-id="f27e8-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="f27e8-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="f27e8-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="f27e8-133">NOTES</span></span>

## <span data-ttu-id="f27e8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f27e8-134">RELATED LINKS</span></span>
