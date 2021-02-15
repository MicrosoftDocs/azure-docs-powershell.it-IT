---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189127"
---
# <span data-ttu-id="7b621-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7b621-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="7b621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b621-102">SYNOPSIS</span></span>
<span data-ttu-id="7b621-103">Ottenere un connettore dati.</span><span class="sxs-lookup"><span data-stu-id="7b621-103">Get a Data Connector.</span></span>

## <span data-ttu-id="7b621-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b621-104">SYNTAX</span></span>

### <span data-ttu-id="7b621-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b621-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b621-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="7b621-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b621-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b621-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b621-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b621-108">DESCRIPTION</span></span>
<span data-ttu-id="7b621-109">Il cmdlet **Get-AzSentinelDataConnector** ottiene un connettore di dati dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="7b621-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="7b621-110">Se si specifica il *parametro DataConnectorId,* viene restituito un singolo **oggetto DataConnector.**</span><span class="sxs-lookup"><span data-stu-id="7b621-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="7b621-111">Se non si specifica il parametro *DataConnectorId,* verrà restituita una matrice contenente tutti i connettori dati nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="7b621-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="7b621-112">È possibile usare **l'oggetto DataConnector** per aggiornare il connettore di dati, ad esempio per disabilitare **DataConnector.**</span><span class="sxs-lookup"><span data-stu-id="7b621-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="7b621-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b621-113">EXAMPLES</span></span>

### <span data-ttu-id="7b621-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b621-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="7b621-115">Questo esempio recupera tutti i **DataConnectors nell'area** di lavoro specificata e quindi li archivia nella $DataConnectors variabile.</span><span class="sxs-lookup"><span data-stu-id="7b621-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="7b621-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7b621-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="7b621-117">Questo esempio recupera un **dataConnector** nell'area di lavoro specificata e quindi lo archivia nella $DataConnector variabile.</span><span class="sxs-lookup"><span data-stu-id="7b621-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="7b621-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b621-118">PARAMETERS</span></span>

### <span data-ttu-id="7b621-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="7b621-119">-DataConnectorId</span></span>
<span data-ttu-id="7b621-120">ID connettore dati.</span><span class="sxs-lookup"><span data-stu-id="7b621-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b621-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b621-121">-DefaultProfile</span></span>
<span data-ttu-id="7b621-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b621-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b621-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b621-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b621-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7b621-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b621-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b621-125">-ResourceId</span></span>
<span data-ttu-id="7b621-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b621-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b621-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7b621-127">-WorkspaceName</span></span>
<span data-ttu-id="7b621-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7b621-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b621-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b621-129">CommonParameters</span></span>
<span data-ttu-id="7b621-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b621-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b621-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b621-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b621-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b621-132">INPUTS</span></span>

### <span data-ttu-id="7b621-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7b621-133">System.String</span></span>
## <span data-ttu-id="7b621-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b621-134">OUTPUTS</span></span>

### <span data-ttu-id="7b621-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="7b621-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="7b621-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b621-136">NOTES</span></span>

## <span data-ttu-id="7b621-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b621-137">RELATED LINKS</span></span>
