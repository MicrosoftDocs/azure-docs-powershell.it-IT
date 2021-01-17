---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486215"
---
# <span data-ttu-id="c0b78-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="c0b78-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="c0b78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0b78-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b78-103">Ottenere un connettore dati.</span><span class="sxs-lookup"><span data-stu-id="c0b78-103">Get a Data Connector.</span></span>

## <span data-ttu-id="c0b78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0b78-104">SYNTAX</span></span>

### <span data-ttu-id="c0b78-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0b78-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0b78-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="c0b78-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0b78-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0b78-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0b78-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0b78-108">DESCRIPTION</span></span>
<span data-ttu-id="c0b78-109">Il cmdlet **Get-AzSentinelDataConnector** ottiene un connettore di dati dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c0b78-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="c0b78-110">Se specifichi il parametro *DataConnectorId* , viene restituito un singolo oggetto **DataConnector** .</span><span class="sxs-lookup"><span data-stu-id="c0b78-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="c0b78-111">Se non specifichi il parametro *DataConnectorId* , viene restituita una matrice contenente tutti i connettori dati nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c0b78-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="c0b78-112">Puoi usare l'oggetto **DataConnector** per **aggiornare il connettore** di dati, ad esempio puoi disabilitare il DataConnector.</span><span class="sxs-lookup"><span data-stu-id="c0b78-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="c0b78-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0b78-113">EXAMPLES</span></span>

### <span data-ttu-id="c0b78-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0b78-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="c0b78-115">Questo esempio recupera tutti i **DataConnector** nell'area di lavoro specificata e lo archivia nella variabile $DataConnectors.</span><span class="sxs-lookup"><span data-stu-id="c0b78-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="c0b78-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c0b78-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="c0b78-117">Questo esempio ottiene un **DataConnector** nell'area di lavoro specificata e lo archivia nella variabile $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="c0b78-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="c0b78-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0b78-118">PARAMETERS</span></span>

### <span data-ttu-id="c0b78-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="c0b78-119">-DataConnectorId</span></span>
<span data-ttu-id="c0b78-120">ID connettore dati.</span><span class="sxs-lookup"><span data-stu-id="c0b78-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="c0b78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b78-121">-DefaultProfile</span></span>
<span data-ttu-id="c0b78-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b78-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b78-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b78-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0b78-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0b78-124">Resource group name.</span></span>

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

### <span data-ttu-id="c0b78-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0b78-125">-ResourceId</span></span>
<span data-ttu-id="c0b78-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0b78-126">Resource Id.</span></span>

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

### <span data-ttu-id="c0b78-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0b78-127">-WorkspaceName</span></span>
<span data-ttu-id="c0b78-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c0b78-128">Workspace Name.</span></span>

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

### <span data-ttu-id="c0b78-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b78-129">CommonParameters</span></span>
<span data-ttu-id="c0b78-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b78-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b78-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0b78-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b78-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0b78-132">INPUTS</span></span>

### <span data-ttu-id="c0b78-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c0b78-133">System.String</span></span>
## <span data-ttu-id="c0b78-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0b78-134">OUTPUTS</span></span>

### <span data-ttu-id="c0b78-135">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="c0b78-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="c0b78-136">Note</span><span class="sxs-lookup"><span data-stu-id="c0b78-136">NOTES</span></span>

## <span data-ttu-id="c0b78-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0b78-137">RELATED LINKS</span></span>
