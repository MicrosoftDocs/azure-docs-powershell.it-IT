---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349291"
---
# <span data-ttu-id="cf03f-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="cf03f-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="cf03f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf03f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf03f-103">Restituisce un elenco di entità di database del cluster e del database kusto specificati.</span><span class="sxs-lookup"><span data-stu-id="cf03f-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="cf03f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf03f-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf03f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf03f-105">DESCRIPTION</span></span>
<span data-ttu-id="cf03f-106">Restituisce un elenco di entità di database del cluster e del database kusto specificati.</span><span class="sxs-lookup"><span data-stu-id="cf03f-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="cf03f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf03f-107">EXAMPLES</span></span>

### <span data-ttu-id="cf03f-108">Esempio 1: elenco delle entità di database del cluster e del database kusto specificati</span><span class="sxs-lookup"><span data-stu-id="cf03f-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="cf03f-109">Il comando precedente restituisce un elenco di entità di database del cluster e del database kusto specificati</span><span class="sxs-lookup"><span data-stu-id="cf03f-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="cf03f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf03f-110">PARAMETERS</span></span>

### <span data-ttu-id="cf03f-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="cf03f-111">-ClusterName</span></span>
<span data-ttu-id="cf03f-112">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="cf03f-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cf03f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf03f-113">-DatabaseName</span></span>
<span data-ttu-id="cf03f-114">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="cf03f-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cf03f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf03f-115">-DefaultProfile</span></span>
<span data-ttu-id="cf03f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf03f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf03f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf03f-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf03f-118">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="cf03f-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cf03f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf03f-119">-SubscriptionId</span></span>
<span data-ttu-id="cf03f-120">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf03f-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf03f-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cf03f-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf03f-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf03f-122">-Confirm</span></span>
<span data-ttu-id="cf03f-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf03f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf03f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf03f-124">-WhatIf</span></span>
<span data-ttu-id="cf03f-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf03f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf03f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf03f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf03f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf03f-127">CommonParameters</span></span>
<span data-ttu-id="cf03f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf03f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf03f-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf03f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf03f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf03f-130">INPUTS</span></span>

## <span data-ttu-id="cf03f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf03f-131">OUTPUTS</span></span>

### <span data-ttu-id="cf03f-132">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="cf03f-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="cf03f-133">Note</span><span class="sxs-lookup"><span data-stu-id="cf03f-133">NOTES</span></span>

<span data-ttu-id="cf03f-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cf03f-134">ALIASES</span></span>

## <span data-ttu-id="cf03f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf03f-135">RELATED LINKS</span></span>

