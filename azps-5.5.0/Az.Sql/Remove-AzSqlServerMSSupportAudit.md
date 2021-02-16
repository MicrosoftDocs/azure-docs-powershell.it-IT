---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197646"
---
# <span data-ttu-id="5c316-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="5c316-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="5c316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c316-102">SYNOPSIS</span></span>
<span data-ttu-id="5c316-103">Rimuove le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5c316-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="5c316-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c316-104">SYNTAX</span></span>

### <span data-ttu-id="5c316-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c316-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c316-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c316-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c316-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5c316-107">DESCRIPTION</span></span>
<span data-ttu-id="5c316-108">Il cmdlet **Remove-AzSqlServerMSSupportAudit** rimuove le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5c316-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="5c316-109">Per usare il cmdlet, usare i *parametri ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="5c316-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="5c316-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c316-110">EXAMPLES</span></span>

### <span data-ttu-id="5c316-111">Esempio 1: Rimuovere le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5c316-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="5c316-112">Esempio 2: Rimuovere tramite pipeline le impostazioni di controllo del supporto Microsoft di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5c316-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="5c316-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c316-113">PARAMETERS</span></span>

### <span data-ttu-id="5c316-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c316-114">-AsJob</span></span>
<span data-ttu-id="5c316-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5c316-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c316-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c316-116">-DefaultProfile</span></span>
<span data-ttu-id="5c316-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c316-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c316-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c316-118">-ResourceGroupName</span></span>
<span data-ttu-id="5c316-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c316-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c316-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c316-120">-ServerName</span></span>
<span data-ttu-id="5c316-121">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="5c316-121">SQL server name.</span></span>

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

### <span data-ttu-id="5c316-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="5c316-122">-ServerObject</span></span>
<span data-ttu-id="5c316-123">Oggetto server per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="5c316-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="5c316-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c316-124">-Confirm</span></span>
<span data-ttu-id="5c316-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c316-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c316-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c316-126">-WhatIf</span></span>
<span data-ttu-id="5c316-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c316-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c316-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c316-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c316-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c316-129">CommonParameters</span></span>
<span data-ttu-id="5c316-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c316-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c316-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c316-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c316-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="5c316-132">INPUTS</span></span>

### <span data-ttu-id="5c316-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5c316-133">System.String</span></span>

### <span data-ttu-id="5c316-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5c316-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="5c316-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c316-135">OUTPUTS</span></span>

### <span data-ttu-id="5c316-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c316-136">System.Boolean</span></span>

## <span data-ttu-id="5c316-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="5c316-137">NOTES</span></span>

## <span data-ttu-id="5c316-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c316-138">RELATED LINKS</span></span>
