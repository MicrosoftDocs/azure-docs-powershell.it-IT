---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 74c5504196a96408d66f8d64391552ebbc4449c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673701"
---
# <span data-ttu-id="ea4b5-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="ea4b5-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="ea4b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4b5-103">Creare un tunnel SSH di Kubectl nel dashboard del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="ea4b5-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="ea4b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea4b5-104">SYNTAX</span></span>

### <span data-ttu-id="ea4b5-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea4b5-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4b5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4b5-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4b5-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea4b5-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea4b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea4b5-108">DESCRIPTION</span></span>
<span data-ttu-id="ea4b5-109">Creare un tunnel SSH di Kubectl nel dashboard del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="ea4b5-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="ea4b5-110">Il tunnel SSH è configurato in un processo di PowerShell denominato Kubectl-Tunnel e può essere trovato eseguendo `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="ea4b5-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="ea4b5-111">Il tunnel deve essere accessibile tramite [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="ea4b5-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="ea4b5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea4b5-112">EXAMPLES</span></span>

### <span data-ttu-id="ea4b5-113">Avviare un tunnel SSH e aprire un browser nel dashboard di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ea4b5-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ea4b5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea4b5-114">PARAMETERS</span></span>

### <span data-ttu-id="ea4b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4b5-115">-DefaultProfile</span></span>
<span data-ttu-id="ea4b5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea4b5-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="ea4b5-117">-DisableBrowser</span></span>
<span data-ttu-id="ea4b5-118">Non aprire un browser dopo aver establising la porta di kubectl in avanti.</span><span class="sxs-lookup"><span data-stu-id="ea4b5-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

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

### <span data-ttu-id="ea4b5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ea4b5-119">-Id</span></span>
<span data-ttu-id="ea4b5-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="ea4b5-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ea4b5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea4b5-121">-InputObject</span></span>
<span data-ttu-id="ea4b5-122">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea4b5-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea4b5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea4b5-123">-Name</span></span>
<span data-ttu-id="ea4b5-124">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="ea4b5-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ea4b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea4b5-125">-PassThru</span></span>
<span data-ttu-id="ea4b5-126">Cmdlet restituisce il KubeTunnelJob se passato.</span><span class="sxs-lookup"><span data-stu-id="ea4b5-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="ea4b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea4b5-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ea4b5-128">Resource group name</span></span>

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

### <span data-ttu-id="ea4b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4b5-129">CommonParameters</span></span>
<span data-ttu-id="ea4b5-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea4b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4b5-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4b5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4b5-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea4b5-132">INPUTS</span></span>

### <span data-ttu-id="ea4b5-133">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ea4b5-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ea4b5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ea4b5-134">System.String</span></span>

## <span data-ttu-id="ea4b5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea4b5-135">OUTPUTS</span></span>

### <span data-ttu-id="ea4b5-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="ea4b5-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="ea4b5-137">Note</span><span class="sxs-lookup"><span data-stu-id="ea4b5-137">NOTES</span></span>

## <span data-ttu-id="ea4b5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea4b5-138">RELATED LINKS</span></span>
