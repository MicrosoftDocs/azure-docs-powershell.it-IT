---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5202f4c86d1d83d6e337c61ee6fc0f72a2b031de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998281"
---
# <span data-ttu-id="f9349-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="f9349-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="f9349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9349-102">SYNOPSIS</span></span>
<span data-ttu-id="f9349-103">Creare un tunnel SSH Kubectl nel dashboard del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="f9349-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="f9349-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9349-104">SYNTAX</span></span>

### <span data-ttu-id="f9349-105">GroupNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="f9349-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9349-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9349-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9349-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9349-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9349-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9349-108">DESCRIPTION</span></span>
<span data-ttu-id="f9349-109">Creare un tunnel SSH Kubectl nel dashboard del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="f9349-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="f9349-110">Il tunnel SSH viene installato in un processo di PowerShell denominato Kubectl-Tunnel e può essere trovato eseguendo `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="f9349-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="f9349-111">Il tunnel deve essere accessibile tramite [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="f9349-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="f9349-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9349-112">EXAMPLES</span></span>

### <span data-ttu-id="f9349-113">Avviare un tunnel SSH e aprire un browser nel dashboard di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="f9349-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f9349-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9349-114">PARAMETERS</span></span>

### <span data-ttu-id="f9349-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9349-115">-DefaultProfile</span></span>
<span data-ttu-id="f9349-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9349-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9349-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="f9349-117">-DisableBrowser</span></span>
<span data-ttu-id="f9349-118">Non aprire un browser dopo aver stabilito la porta di inoltro del kubectl.</span><span class="sxs-lookup"><span data-stu-id="f9349-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9349-119">-Id</span><span class="sxs-lookup"><span data-stu-id="f9349-119">-Id</span></span>
<span data-ttu-id="f9349-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="f9349-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9349-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9349-121">-InputObject</span></span>
<span data-ttu-id="f9349-122">Oggetto PSKubernetesCluster, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="f9349-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9349-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="f9349-123">-ListenPort</span></span>
<span data-ttu-id="f9349-124">La porta di ascolto per il dashboard.</span><span class="sxs-lookup"><span data-stu-id="f9349-124">The listening port for the dashboard.</span></span> <span data-ttu-id="f9349-125">Il valore predefinito è 8003.</span><span class="sxs-lookup"><span data-stu-id="f9349-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9349-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f9349-126">-Name</span></span>
<span data-ttu-id="f9349-127">Nome del cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="f9349-127">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9349-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9349-128">-PassThru</span></span>
<span data-ttu-id="f9349-129">Il cmdlet restituisce KubeTunnelJob se è stato passato.</span><span class="sxs-lookup"><span data-stu-id="f9349-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9349-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9349-130">-ResourceGroupName</span></span>
<span data-ttu-id="f9349-131">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f9349-131">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9349-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9349-132">CommonParameters</span></span>
<span data-ttu-id="f9349-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9349-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9349-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9349-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9349-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9349-135">INPUTS</span></span>

### <span data-ttu-id="f9349-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f9349-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="f9349-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f9349-137">System.String</span></span>

## <span data-ttu-id="f9349-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9349-138">OUTPUTS</span></span>

### <span data-ttu-id="f9349-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="f9349-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="f9349-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9349-140">NOTES</span></span>

## <span data-ttu-id="f9349-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9349-141">RELATED LINKS</span></span>
