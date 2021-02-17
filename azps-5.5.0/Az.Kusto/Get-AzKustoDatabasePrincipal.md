---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185223"
---
# <span data-ttu-id="7a49f-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="7a49f-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="7a49f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a49f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a49f-103">Restituisce un elenco delle entità database del cluster e database Kusto specificato.</span><span class="sxs-lookup"><span data-stu-id="7a49f-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="7a49f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a49f-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a49f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7a49f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a49f-106">Restituisce un elenco delle entità database del cluster e database Kusto specificato.</span><span class="sxs-lookup"><span data-stu-id="7a49f-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="7a49f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a49f-107">EXAMPLES</span></span>

### <span data-ttu-id="7a49f-108">Esempio 1: Elenco delle entità database del cluster e del database Kusto specificato</span><span class="sxs-lookup"><span data-stu-id="7a49f-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="7a49f-109">Il comando precedente restituisce un elenco delle entità database del cluster e del database Kusto specificato</span><span class="sxs-lookup"><span data-stu-id="7a49f-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="7a49f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a49f-110">PARAMETERS</span></span>

### <span data-ttu-id="7a49f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a49f-111">-ClusterName</span></span>
<span data-ttu-id="7a49f-112">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a49f-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7a49f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a49f-113">-DatabaseName</span></span>
<span data-ttu-id="7a49f-114">Nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a49f-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="7a49f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a49f-115">-DefaultProfile</span></span>
<span data-ttu-id="7a49f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a49f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a49f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a49f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a49f-118">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a49f-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7a49f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a49f-119">-SubscriptionId</span></span>
<span data-ttu-id="7a49f-120">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7a49f-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7a49f-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7a49f-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7a49f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a49f-122">-Confirm</span></span>
<span data-ttu-id="7a49f-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a49f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a49f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a49f-124">-WhatIf</span></span>
<span data-ttu-id="7a49f-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a49f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a49f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a49f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a49f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a49f-127">CommonParameters</span></span>
<span data-ttu-id="7a49f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a49f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a49f-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a49f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a49f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="7a49f-130">INPUTS</span></span>

## <span data-ttu-id="7a49f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a49f-131">OUTPUTS</span></span>

### <span data-ttu-id="7a49f-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="7a49f-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="7a49f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="7a49f-133">NOTES</span></span>

<span data-ttu-id="7a49f-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7a49f-134">ALIASES</span></span>

## <span data-ttu-id="7a49f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a49f-135">RELATED LINKS</span></span>

