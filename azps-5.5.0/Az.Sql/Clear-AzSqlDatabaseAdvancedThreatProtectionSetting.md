---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178526"
---
# <span data-ttu-id="b0fc9-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b0fc9-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="b0fc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fc9-103">Rimuove le impostazioni di Protezione avanzata dalle minacce da un database.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="b0fc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0fc9-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0fc9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="b0fc9-106">Il cmdlet **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** rimuove le impostazioni di Protezione avanzata dalle minacce da un database SQL AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="b0fc9-107">Per usare questo cmdlet, specificare i *parametri ResourceGroupName* e *ServerName* per identificare il database da cui il cmdlet rimuove le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="b0fc9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0fc9-108">EXAMPLES</span></span>

### <span data-ttu-id="b0fc9-109">Esempio 1: Rimuovere le impostazioni di Protezione avanzata dalle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="b0fc9-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b0fc9-110">Questo comando rimuove le impostazioni di Protezione avanzata dalle minacce da un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="b0fc9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0fc9-111">PARAMETERS</span></span>

### <span data-ttu-id="b0fc9-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0fc9-112">-DatabaseName</span></span>
<span data-ttu-id="b0fc9-113">Specifica il nome di un database in cui devono essere rimosse le impostazioni di Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0fc9-114">-DefaultProfile</span></span>
<span data-ttu-id="b0fc9-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b0fc9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0fc9-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0fc9-116">-PassThru</span></span>
<span data-ttu-id="b0fc9-117">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b0fc9-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b0fc9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0fc9-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0fc9-120">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="b0fc9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0fc9-121">-ServerName</span></span>
<span data-ttu-id="b0fc9-122">Specifica il nome di un server in cui viene eseguito il database.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-122">Specifies the name of a server on which the database runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fc9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0fc9-123">-Confirm</span></span>
<span data-ttu-id="b0fc9-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0fc9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0fc9-125">-WhatIf</span></span>
<span data-ttu-id="b0fc9-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0fc9-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0fc9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fc9-128">CommonParameters</span></span>
<span data-ttu-id="b0fc9-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fc9-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0fc9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fc9-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0fc9-131">INPUTS</span></span>

### <span data-ttu-id="b0fc9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b0fc9-132">System.String</span></span>

## <span data-ttu-id="b0fc9-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0fc9-133">OUTPUTS</span></span>

### <span data-ttu-id="b0fc9-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="b0fc9-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="b0fc9-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0fc9-135">NOTES</span></span>

## <span data-ttu-id="b0fc9-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0fc9-136">RELATED LINKS</span></span>

[<span data-ttu-id="b0fc9-137">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="b0fc9-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


