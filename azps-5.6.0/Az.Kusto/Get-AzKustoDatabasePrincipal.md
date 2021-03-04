---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 3380835b4ca8e51c8ba0952ef3ef4bd973fadea3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952462"
---
# <span data-ttu-id="4617b-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="4617b-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="4617b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4617b-102">SYNOPSIS</span></span>
<span data-ttu-id="4617b-103">Restituisce un elenco delle entità database del cluster e database Kusto specificato.</span><span class="sxs-lookup"><span data-stu-id="4617b-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="4617b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4617b-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4617b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4617b-105">DESCRIPTION</span></span>
<span data-ttu-id="4617b-106">Restituisce un elenco delle entità database del cluster e database Kusto specificato.</span><span class="sxs-lookup"><span data-stu-id="4617b-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="4617b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4617b-107">EXAMPLES</span></span>

### <span data-ttu-id="4617b-108">Esempio 1: Elenco delle entità database del cluster e del database Kusto specificato</span><span class="sxs-lookup"><span data-stu-id="4617b-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="4617b-109">Il comando precedente restituisce un elenco delle entità database del cluster e del database Kusto specificato</span><span class="sxs-lookup"><span data-stu-id="4617b-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="4617b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4617b-110">PARAMETERS</span></span>

### <span data-ttu-id="4617b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4617b-111">-ClusterName</span></span>
<span data-ttu-id="4617b-112">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4617b-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4617b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4617b-113">-DatabaseName</span></span>
<span data-ttu-id="4617b-114">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4617b-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="4617b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4617b-115">-DefaultProfile</span></span>
<span data-ttu-id="4617b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4617b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4617b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4617b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4617b-118">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4617b-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4617b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4617b-119">-SubscriptionId</span></span>
<span data-ttu-id="4617b-120">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4617b-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4617b-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4617b-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4617b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4617b-122">-Confirm</span></span>
<span data-ttu-id="4617b-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4617b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4617b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4617b-124">-WhatIf</span></span>
<span data-ttu-id="4617b-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4617b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4617b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4617b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4617b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4617b-127">CommonParameters</span></span>
<span data-ttu-id="4617b-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4617b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4617b-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4617b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4617b-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="4617b-130">INPUTS</span></span>

## <span data-ttu-id="4617b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4617b-131">OUTPUTS</span></span>

### <span data-ttu-id="4617b-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="4617b-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="4617b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="4617b-133">NOTES</span></span>

<span data-ttu-id="4617b-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4617b-134">ALIASES</span></span>

## <span data-ttu-id="4617b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4617b-135">RELATED LINKS</span></span>

