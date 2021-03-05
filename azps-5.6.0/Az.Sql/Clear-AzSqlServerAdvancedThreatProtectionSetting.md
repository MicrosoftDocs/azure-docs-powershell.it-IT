---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4a576c930d8ff1c53c6c9e92c7d87664aef4da4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011598"
---
# <span data-ttu-id="e563a-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e563a-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e563a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e563a-102">SYNOPSIS</span></span>
<span data-ttu-id="e563a-103">Rimuove le impostazioni di Protezione avanzata dalle minacce da un server.</span><span class="sxs-lookup"><span data-stu-id="e563a-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="e563a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e563a-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e563a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e563a-105">DESCRIPTION</span></span>
<span data-ttu-id="e563a-106">Il cmdlet Clear-AzSqlServerAdvancedThreatProtectionSetting rimuove le impostazioni di Protezione avanzata dalle minacce da un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e563a-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="e563a-107">Per usare questo cmdlet, specificare i parametri ResourceGroupName e ServerName per identificare il server da cui il cmdlet rimuove le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e563a-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="e563a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e563a-108">EXAMPLES</span></span>

### <span data-ttu-id="e563a-109">Esempio 1: Rimuovere le impostazioni di Protezione avanzata dalle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="e563a-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="e563a-110">Questo comando rimuove le impostazioni di Protezione avanzata dalle minacce da un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="e563a-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="e563a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e563a-111">PARAMETERS</span></span>

### <span data-ttu-id="e563a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e563a-112">-DefaultProfile</span></span>
<span data-ttu-id="e563a-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e563a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e563a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e563a-114">-PassThru</span></span>
<span data-ttu-id="e563a-115">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e563a-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e563a-116">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e563a-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e563a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e563a-117">-ResourceGroupName</span></span>
<span data-ttu-id="e563a-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="e563a-118">Specifies the name of the resource group the server is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e563a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e563a-119">-ServerName</span></span>
<span data-ttu-id="e563a-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="e563a-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e563a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e563a-121">-Confirm</span></span>
<span data-ttu-id="e563a-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e563a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e563a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e563a-123">-WhatIf</span></span>
<span data-ttu-id="e563a-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e563a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e563a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e563a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e563a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e563a-126">CommonParameters</span></span>
<span data-ttu-id="e563a-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e563a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e563a-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e563a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e563a-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e563a-129">INPUTS</span></span>

### <span data-ttu-id="e563a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e563a-130">System.String</span></span>

## <span data-ttu-id="e563a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e563a-131">OUTPUTS</span></span>

### <span data-ttu-id="e563a-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="e563a-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="e563a-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="e563a-133">NOTES</span></span>

## <span data-ttu-id="e563a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e563a-134">RELATED LINKS</span></span>

[<span data-ttu-id="e563a-135">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="e563a-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

