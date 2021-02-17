---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176774"
---
# <span data-ttu-id="737a1-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="737a1-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="737a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737a1-102">SYNOPSIS</span></span>
<span data-ttu-id="737a1-103">Rimuove le impostazioni di controllo di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="737a1-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="737a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="737a1-104">SYNTAX</span></span>

### <span data-ttu-id="737a1-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="737a1-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="737a1-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="737a1-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="737a1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="737a1-107">DESCRIPTION</span></span>
<span data-ttu-id="737a1-108">Il cmdlet **Remove-AzSqlServerAudit** rimuove le impostazioni di controllo di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="737a1-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="737a1-109">Specificare i *parametri ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="737a1-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="737a1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="737a1-110">EXAMPLES</span></span>

### <span data-ttu-id="737a1-111">Esempio 1: Rimuovere le impostazioni di controllo di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="737a1-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="737a1-112">Esempio 2: Rimuovere tramite pipeline le impostazioni di controllo di un server di SQL Azure</span><span class="sxs-lookup"><span data-stu-id="737a1-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="737a1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="737a1-113">PARAMETERS</span></span>

### <span data-ttu-id="737a1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="737a1-114">-AsJob</span></span>
<span data-ttu-id="737a1-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="737a1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="737a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737a1-116">-DefaultProfile</span></span>
<span data-ttu-id="737a1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="737a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737a1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737a1-118">-ResourceGroupName</span></span>
<span data-ttu-id="737a1-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="737a1-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a1-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="737a1-120">-ServerName</span></span>
<span data-ttu-id="737a1-121">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="737a1-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a1-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="737a1-122">-ServerObject</span></span>
<span data-ttu-id="737a1-123">Oggetto server per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="737a1-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="737a1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="737a1-124">-Confirm</span></span>
<span data-ttu-id="737a1-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737a1-126">-WhatIf</span></span>
<span data-ttu-id="737a1-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="737a1-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="737a1-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="737a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737a1-129">CommonParameters</span></span>
<span data-ttu-id="737a1-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737a1-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="737a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737a1-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="737a1-132">INPUTS</span></span>

### <span data-ttu-id="737a1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="737a1-133">System.String</span></span>

### <span data-ttu-id="737a1-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="737a1-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="737a1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="737a1-135">OUTPUTS</span></span>

### <span data-ttu-id="737a1-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="737a1-136">System.Boolean</span></span>

## <span data-ttu-id="737a1-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="737a1-137">NOTES</span></span>

## <span data-ttu-id="737a1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="737a1-138">RELATED LINKS</span></span>
