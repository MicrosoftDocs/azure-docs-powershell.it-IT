---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188334"
---
# <span data-ttu-id="dd765-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd765-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="dd765-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd765-102">SYNOPSIS</span></span>
<span data-ttu-id="dd765-103">Eliminare l'account di archiviazione collegata per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="dd765-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="dd765-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd765-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd765-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd765-105">DESCRIPTION</span></span>
<span data-ttu-id="dd765-106">Eliminare l'account di archiviazione collegata per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="dd765-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="dd765-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd765-107">EXAMPLES</span></span>

### <span data-ttu-id="dd765-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd765-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="dd765-109">Eliminare l'account di archiviazione collegata con il tipo "CustomLogs" per {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="dd765-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="dd765-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd765-110">PARAMETERS</span></span>

### <span data-ttu-id="dd765-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="dd765-111">-DataSourceType</span></span>
<span data-ttu-id="dd765-112">Il tipo di origine dati deve essere uno di "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="dd765-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd765-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd765-113">-DefaultProfile</span></span>
<span data-ttu-id="dd765-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd765-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd765-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dd765-115">-Force</span></span>
<span data-ttu-id="dd765-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dd765-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dd765-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd765-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd765-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd765-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd765-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dd765-119">-WorkspaceName</span></span>
<span data-ttu-id="dd765-120">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="dd765-120">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd765-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd765-121">-Confirm</span></span>
<span data-ttu-id="dd765-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd765-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd765-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd765-123">-WhatIf</span></span>
<span data-ttu-id="dd765-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd765-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd765-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd765-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd765-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd765-126">CommonParameters</span></span>
<span data-ttu-id="dd765-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd765-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd765-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd765-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd765-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd765-129">INPUTS</span></span>

### <span data-ttu-id="dd765-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dd765-130">System.String</span></span>

## <span data-ttu-id="dd765-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd765-131">OUTPUTS</span></span>

### <span data-ttu-id="dd765-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd765-132">System.Boolean</span></span>

## <span data-ttu-id="dd765-133">Note</span><span class="sxs-lookup"><span data-stu-id="dd765-133">NOTES</span></span>

## <span data-ttu-id="dd765-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd765-134">RELATED LINKS</span></span>
