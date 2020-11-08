---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199993"
---
# <span data-ttu-id="e7c4a-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e7c4a-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="e7c4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c4a-103">Rimuove un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="e7c4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7c4a-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7c4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c4a-106">Il cmdlet **Remove-AzSqlServer** rimuove un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="e7c4a-107">L'operazione di eliminazione è asincrona e può richiedere del tempo, quindi verificare che l'operazione sia terminata prima di eseguire altre operazioni che dipendono dal server che viene completamente eliminato.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="e7c4a-108">Ad esempio, devi creare un nuovo server che usa lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="e7c4a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7c4a-109">EXAMPLES</span></span>

### <span data-ttu-id="e7c4a-110">Esempio 1: rimuovere un server</span><span class="sxs-lookup"><span data-stu-id="e7c4a-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e7c4a-111">Questo comando rimuove il server di database SQL di Azure denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="e7c4a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7c4a-112">PARAMETERS</span></span>

### <span data-ttu-id="e7c4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c4a-113">-DefaultProfile</span></span>
<span data-ttu-id="e7c4a-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e7c4a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7c4a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e7c4a-115">-Force</span></span>
<span data-ttu-id="e7c4a-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7c4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7c4a-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e7c4a-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e7c4a-119">-ServerName</span></span>
<span data-ttu-id="e7c4a-120">Specifica il nome del server da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c4a-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e7c4a-121">-Confirm</span></span>
<span data-ttu-id="e7c4a-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c4a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c4a-123">-WhatIf</span></span>
<span data-ttu-id="e7c4a-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c4a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c4a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c4a-126">CommonParameters</span></span>
<span data-ttu-id="e7c4a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c4a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c4a-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7c4a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c4a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7c4a-129">INPUTS</span></span>

### <span data-ttu-id="e7c4a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e7c4a-130">System.String</span></span>

## <span data-ttu-id="e7c4a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7c4a-131">OUTPUTS</span></span>

### <span data-ttu-id="e7c4a-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e7c4a-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e7c4a-133">Note</span><span class="sxs-lookup"><span data-stu-id="e7c4a-133">NOTES</span></span>

## <span data-ttu-id="e7c4a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7c4a-134">RELATED LINKS</span></span>

[<span data-ttu-id="e7c4a-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e7c4a-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="e7c4a-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e7c4a-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e7c4a-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e7c4a-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="e7c4a-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="e7c4a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


