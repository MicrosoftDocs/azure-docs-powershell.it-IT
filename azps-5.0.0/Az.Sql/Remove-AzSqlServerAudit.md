---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193146"
---
# <span data-ttu-id="588a0-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="588a0-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="588a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="588a0-102">SYNOPSIS</span></span>
<span data-ttu-id="588a0-103">Rimuove le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="588a0-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="588a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="588a0-104">SYNTAX</span></span>

### <span data-ttu-id="588a0-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="588a0-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588a0-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="588a0-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="588a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="588a0-107">DESCRIPTION</span></span>
<span data-ttu-id="588a0-108">Il cmdlet **Remove-AzSqlServerAudit** rimuove le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="588a0-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="588a0-109">Specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="588a0-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="588a0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="588a0-110">EXAMPLES</span></span>

### <span data-ttu-id="588a0-111">Esempio 1: rimuovere le impostazioni di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="588a0-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="588a0-112">Esempio 2: rimuovere, tramite pipeline, le impostazioni di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="588a0-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="588a0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="588a0-113">PARAMETERS</span></span>

### <span data-ttu-id="588a0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="588a0-114">-AsJob</span></span>
<span data-ttu-id="588a0-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="588a0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="588a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588a0-116">-DefaultProfile</span></span>
<span data-ttu-id="588a0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="588a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="588a0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="588a0-118">-ResourceGroupName</span></span>
<span data-ttu-id="588a0-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="588a0-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="588a0-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="588a0-120">-ServerName</span></span>
<span data-ttu-id="588a0-121">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="588a0-121">SQL server name.</span></span>

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

### <span data-ttu-id="588a0-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="588a0-122">-ServerObject</span></span>
<span data-ttu-id="588a0-123">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="588a0-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="588a0-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="588a0-124">-Confirm</span></span>
<span data-ttu-id="588a0-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="588a0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="588a0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="588a0-126">-WhatIf</span></span>
<span data-ttu-id="588a0-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="588a0-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="588a0-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="588a0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="588a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588a0-129">CommonParameters</span></span>
<span data-ttu-id="588a0-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588a0-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="588a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588a0-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="588a0-132">INPUTS</span></span>

### <span data-ttu-id="588a0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="588a0-133">System.String</span></span>

### <span data-ttu-id="588a0-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="588a0-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="588a0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="588a0-135">OUTPUTS</span></span>

### <span data-ttu-id="588a0-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="588a0-136">System.Boolean</span></span>

## <span data-ttu-id="588a0-137">Note</span><span class="sxs-lookup"><span data-stu-id="588a0-137">NOTES</span></span>

## <span data-ttu-id="588a0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="588a0-138">RELATED LINKS</span></span>