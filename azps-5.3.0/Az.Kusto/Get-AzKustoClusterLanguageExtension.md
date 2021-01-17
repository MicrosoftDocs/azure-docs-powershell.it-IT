---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 8ad074cf40074032fbab46cab6ee6c6c290eb2ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474124"
---
# <span data-ttu-id="35952-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="35952-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="35952-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35952-102">SYNOPSIS</span></span>
<span data-ttu-id="35952-103">Restituisce un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="35952-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="35952-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35952-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35952-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35952-105">DESCRIPTION</span></span>
<span data-ttu-id="35952-106">Restituisce un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="35952-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="35952-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35952-107">EXAMPLES</span></span>

### <span data-ttu-id="35952-108">Esempio 1: elencare tutte le estensioni di lingua impostate per un cluster</span><span class="sxs-lookup"><span data-stu-id="35952-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="35952-109">Il comando precedente restituisce un elenco di estensioni di lingua che possono essere eseguite in query KQL.</span><span class="sxs-lookup"><span data-stu-id="35952-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="35952-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35952-110">PARAMETERS</span></span>

### <span data-ttu-id="35952-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="35952-111">-ClusterName</span></span>
<span data-ttu-id="35952-112">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="35952-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35952-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35952-113">-DefaultProfile</span></span>
<span data-ttu-id="35952-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35952-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35952-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35952-115">-ResourceGroupName</span></span>
<span data-ttu-id="35952-116">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="35952-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35952-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35952-117">-SubscriptionId</span></span>
<span data-ttu-id="35952-118">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35952-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35952-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="35952-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35952-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35952-120">-Confirm</span></span>
<span data-ttu-id="35952-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35952-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35952-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35952-122">-WhatIf</span></span>
<span data-ttu-id="35952-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35952-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35952-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35952-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35952-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35952-125">CommonParameters</span></span>
<span data-ttu-id="35952-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35952-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35952-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35952-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35952-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35952-128">INPUTS</span></span>

## <span data-ttu-id="35952-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35952-129">OUTPUTS</span></span>

### <span data-ttu-id="35952-130">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="35952-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="35952-131">Note</span><span class="sxs-lookup"><span data-stu-id="35952-131">NOTES</span></span>

<span data-ttu-id="35952-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="35952-132">ALIASES</span></span>

## <span data-ttu-id="35952-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35952-133">RELATED LINKS</span></span>

