---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: 5858a1f17bcae3c003ed7b40200c065c36eb2b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686758"
---
# <span data-ttu-id="1ba8d-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="1ba8d-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="1ba8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ba8d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba8d-103">Creare un tunnel SSH di Kubectl nel dashboard del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="1ba8d-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ba8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ba8d-104">SYNTAX</span></span>

### <span data-ttu-id="1ba8d-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ba8d-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ba8d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba8d-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ba8d-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba8d-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ba8d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ba8d-108">DESCRIPTION</span></span>
<span data-ttu-id="1ba8d-109">Creare un tunnel SSH di Kubectl nel dashboard del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="1ba8d-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="1ba8d-110">Il tunnel SSH è configurato in un processo di PowerShell denominato Kubectl-Tunnel e può essere trovato eseguendo `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="1ba8d-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="1ba8d-111">Il tunnel deve essere accessibile tramite [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="1ba8d-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="1ba8d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ba8d-112">EXAMPLES</span></span>

### <span data-ttu-id="1ba8d-113">Avviare un tunnel SSH e aprire un browser nel dashboard di Kubernetes</span><span class="sxs-lookup"><span data-stu-id="1ba8d-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="1ba8d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ba8d-114">PARAMETERS</span></span>

### <span data-ttu-id="1ba8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba8d-115">-DefaultProfile</span></span>
<span data-ttu-id="1ba8d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ba8d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba8d-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="1ba8d-117">-DisableBrowser</span></span>
<span data-ttu-id="1ba8d-118">Non aprire un browser dopo aver establising la porta di kubectl in avanti.</span><span class="sxs-lookup"><span data-stu-id="1ba8d-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba8d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="1ba8d-119">-Id</span></span>
<span data-ttu-id="1ba8d-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="1ba8d-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ba8d-121">-InputObject</span></span>
<span data-ttu-id="1ba8d-122">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ba8d-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba8d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ba8d-123">-Name</span></span>
<span data-ttu-id="1ba8d-124">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="1ba8d-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ba8d-125">-PassThru</span></span>
<span data-ttu-id="1ba8d-126">Cmdlet restituisce il KubeTunnelJob se passato.</span><span class="sxs-lookup"><span data-stu-id="1ba8d-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1ba8d-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1ba8d-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba8d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba8d-129">CommonParameters</span></span>
<span data-ttu-id="1ba8d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba8d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba8d-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba8d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba8d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ba8d-132">INPUTS</span></span>

### <span data-ttu-id="1ba8d-133">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1ba8d-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="1ba8d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1ba8d-134">System.String</span></span>

## <span data-ttu-id="1ba8d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ba8d-135">OUTPUTS</span></span>

### <span data-ttu-id="1ba8d-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="1ba8d-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="1ba8d-137">Note</span><span class="sxs-lookup"><span data-stu-id="1ba8d-137">NOTES</span></span>

## <span data-ttu-id="1ba8d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ba8d-138">RELATED LINKS</span></span>
