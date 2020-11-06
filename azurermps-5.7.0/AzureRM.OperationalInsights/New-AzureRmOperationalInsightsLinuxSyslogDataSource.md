---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 49d465b1d993542790c20833ff5b1f75e03d5f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521868"
---
# <span data-ttu-id="9ff89-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="9ff89-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="9ff89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ff89-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff89-103">Aggiunge un'origine dati ai computer Linux.</span><span class="sxs-lookup"><span data-stu-id="9ff89-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ff89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ff89-104">SYNTAX</span></span>

### <span data-ttu-id="9ff89-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ff89-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff89-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9ff89-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff89-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ff89-107">DESCRIPTION</span></span>
<span data-ttu-id="9ff89-108">Il cmdlet **New-AzureRmOperationalInsightsLinuxSyslogDataSource** aggiunge un'origine dati syslog ai computer Linux collegati in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9ff89-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="9ff89-109">Le informazioni operative di Azure possono raccogliere dati syslog.</span><span class="sxs-lookup"><span data-stu-id="9ff89-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="9ff89-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ff89-110">EXAMPLES</span></span>

## <span data-ttu-id="9ff89-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ff89-111">PARAMETERS</span></span>

### <span data-ttu-id="9ff89-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="9ff89-112">-CollectAlert</span></span>
<span data-ttu-id="9ff89-113">Indica che gli approfondimenti operativi raccolgono i messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="9ff89-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="9ff89-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="9ff89-114">-CollectCritical</span></span>
<span data-ttu-id="9ff89-115">Indica che gli approfondimenti operativi raccolgono messaggi critici.</span><span class="sxs-lookup"><span data-stu-id="9ff89-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="9ff89-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="9ff89-116">-CollectDebug</span></span>
<span data-ttu-id="9ff89-117">Indica che gli approfondimenti operativi raccolgono i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="9ff89-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="9ff89-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="9ff89-118">-CollectEmergency</span></span>
<span data-ttu-id="9ff89-119">Indica che gli approfondimenti operativi raccolgono messaggi di emergenza.</span><span class="sxs-lookup"><span data-stu-id="9ff89-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="9ff89-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="9ff89-120">-CollectError</span></span>
<span data-ttu-id="9ff89-121">Indica che gli approfondimenti operativi raccolgono i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="9ff89-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="9ff89-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="9ff89-122">-CollectInformational</span></span>
<span data-ttu-id="9ff89-123">Indica che gli approfondimenti operativi raccolgono i messaggi informativi.</span><span class="sxs-lookup"><span data-stu-id="9ff89-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="9ff89-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="9ff89-124">-CollectNotice</span></span>
<span data-ttu-id="9ff89-125">Indica che gli approfondimenti operativi raccolgono i messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="9ff89-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="9ff89-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="9ff89-126">-CollectWarning</span></span>
<span data-ttu-id="9ff89-127">Indica che il syslog include messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="9ff89-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="9ff89-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff89-128">-DefaultProfile</span></span>
<span data-ttu-id="9ff89-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9ff89-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ff89-130">-Struttura</span><span class="sxs-lookup"><span data-stu-id="9ff89-130">-Facility</span></span>
<span data-ttu-id="9ff89-131">Specifica un codice di struttura.</span><span class="sxs-lookup"><span data-stu-id="9ff89-131">Specifies a facility code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff89-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9ff89-132">-Force</span></span>
<span data-ttu-id="9ff89-133">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9ff89-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ff89-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ff89-134">-Name</span></span>
<span data-ttu-id="9ff89-135">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="9ff89-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="9ff89-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff89-136">-ResourceGroupName</span></span>
<span data-ttu-id="9ff89-137">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="9ff89-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="9ff89-138">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="9ff89-138">-Workspace</span></span>
<span data-ttu-id="9ff89-139">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff89-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9ff89-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ff89-140">-WorkspaceName</span></span>
<span data-ttu-id="9ff89-141">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff89-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9ff89-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ff89-142">-Confirm</span></span>
<span data-ttu-id="9ff89-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff89-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff89-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff89-144">-WhatIf</span></span>
<span data-ttu-id="9ff89-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ff89-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff89-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ff89-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff89-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff89-147">CommonParameters</span></span>
<span data-ttu-id="9ff89-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff89-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff89-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff89-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff89-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ff89-150">INPUTS</span></span>

### <span data-ttu-id="9ff89-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ff89-151">PSWorkspace</span></span>
<span data-ttu-id="9ff89-152">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9ff89-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="9ff89-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ff89-153">OUTPUTS</span></span>

### <span data-ttu-id="9ff89-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9ff89-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9ff89-155">Note</span><span class="sxs-lookup"><span data-stu-id="9ff89-155">NOTES</span></span>

## <span data-ttu-id="9ff89-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ff89-156">RELATED LINKS</span></span>

[<span data-ttu-id="9ff89-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9ff89-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="9ff89-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9ff89-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


