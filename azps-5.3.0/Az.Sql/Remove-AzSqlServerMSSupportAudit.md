---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473769"
---
# <span data-ttu-id="1f08f-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="1f08f-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="1f08f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f08f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f08f-103">Rimuove le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f08f-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="1f08f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f08f-104">SYNTAX</span></span>

### <span data-ttu-id="1f08f-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f08f-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f08f-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f08f-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f08f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f08f-107">DESCRIPTION</span></span>
<span data-ttu-id="1f08f-108">Il cmdlet **Remove-AzSqlServerMSSupportAudit** rimuove le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f08f-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1f08f-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="1f08f-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="1f08f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f08f-110">EXAMPLES</span></span>

### <span data-ttu-id="1f08f-111">Esempio 1: rimuovere le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="1f08f-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="1f08f-112">Esempio 2: rimuovere, tramite pipeline, le impostazioni di controllo del supporto Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="1f08f-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="1f08f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f08f-113">PARAMETERS</span></span>

### <span data-ttu-id="1f08f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f08f-114">-AsJob</span></span>
<span data-ttu-id="1f08f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1f08f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f08f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f08f-116">-DefaultProfile</span></span>
<span data-ttu-id="1f08f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f08f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f08f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f08f-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f08f-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f08f-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f08f-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1f08f-120">-ServerName</span></span>
<span data-ttu-id="1f08f-121">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f08f-121">SQL server name.</span></span>

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

### <span data-ttu-id="1f08f-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="1f08f-122">-ServerObject</span></span>
<span data-ttu-id="1f08f-123">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="1f08f-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="1f08f-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f08f-124">-Confirm</span></span>
<span data-ttu-id="1f08f-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f08f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f08f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f08f-126">-WhatIf</span></span>
<span data-ttu-id="1f08f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f08f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f08f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f08f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f08f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f08f-129">CommonParameters</span></span>
<span data-ttu-id="1f08f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f08f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f08f-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f08f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f08f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f08f-132">INPUTS</span></span>

### <span data-ttu-id="1f08f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f08f-133">System.String</span></span>

### <span data-ttu-id="1f08f-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1f08f-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1f08f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f08f-135">OUTPUTS</span></span>

### <span data-ttu-id="1f08f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f08f-136">System.Boolean</span></span>

## <span data-ttu-id="1f08f-137">Note</span><span class="sxs-lookup"><span data-stu-id="1f08f-137">NOTES</span></span>

## <span data-ttu-id="1f08f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f08f-138">RELATED LINKS</span></span>
