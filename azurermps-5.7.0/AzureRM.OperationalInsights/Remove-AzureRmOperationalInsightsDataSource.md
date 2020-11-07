---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: a3f650861f70ad9110f4716e5034cd5e7f930343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687623"
---
# <span data-ttu-id="cdeaf-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cdeaf-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="cdeaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdeaf-102">SYNOPSIS</span></span>
<span data-ttu-id="cdeaf-103">Elimina un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdeaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdeaf-104">SYNTAX</span></span>

### <span data-ttu-id="cdeaf-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdeaf-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdeaf-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cdeaf-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdeaf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdeaf-107">DESCRIPTION</span></span>
<span data-ttu-id="cdeaf-108">Il cmdlet **Remove-AzureRmOperationalInsightsDataSource** Elimina un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="cdeaf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdeaf-109">EXAMPLES</span></span>

## <span data-ttu-id="cdeaf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdeaf-110">PARAMETERS</span></span>

### <span data-ttu-id="cdeaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdeaf-111">-DefaultProfile</span></span>
<span data-ttu-id="cdeaf-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cdeaf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdeaf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cdeaf-113">-Force</span></span>
<span data-ttu-id="cdeaf-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdeaf-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdeaf-115">-Name</span></span>
<span data-ttu-id="cdeaf-116">Specifica il nome di un'origine dati da eliminare.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdeaf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdeaf-117">-ResourceGroupName</span></span>
<span data-ttu-id="cdeaf-118">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdeaf-119">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="cdeaf-119">-Workspace</span></span>
<span data-ttu-id="cdeaf-120">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdeaf-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cdeaf-121">-WorkspaceName</span></span>
<span data-ttu-id="cdeaf-122">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdeaf-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdeaf-123">-Confirm</span></span>
<span data-ttu-id="cdeaf-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdeaf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdeaf-125">-WhatIf</span></span>
<span data-ttu-id="cdeaf-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdeaf-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdeaf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdeaf-128">CommonParameters</span></span>
<span data-ttu-id="cdeaf-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdeaf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdeaf-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdeaf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdeaf-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdeaf-131">INPUTS</span></span>

### <span data-ttu-id="cdeaf-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cdeaf-132">PSWorkspace</span></span>
<span data-ttu-id="cdeaf-133">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cdeaf-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="cdeaf-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdeaf-134">OUTPUTS</span></span>

## <span data-ttu-id="cdeaf-135">Note</span><span class="sxs-lookup"><span data-stu-id="cdeaf-135">NOTES</span></span>
* <span data-ttu-id="cdeaf-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="cdeaf-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cdeaf-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdeaf-137">RELATED LINKS</span></span>

[<span data-ttu-id="cdeaf-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cdeaf-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="cdeaf-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cdeaf-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


