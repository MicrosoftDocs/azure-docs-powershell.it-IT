---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: ed6f1c2a689ed122ac16004b80f2ab0f0ea2ea3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995174"
---
# <span data-ttu-id="bb37c-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bb37c-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="bb37c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb37c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb37c-103">Elimina un collegamento di comunicazione per le transazioni di database elastiche tra due server.</span><span class="sxs-lookup"><span data-stu-id="bb37c-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="bb37c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb37c-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb37c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb37c-105">DESCRIPTION</span></span>
<span data-ttu-id="bb37c-106">Il cmdlet **Remove-AzSqlServerCommunicationLink** elimina un collegamento di comunicazione da server a server per le transazioni di database elastiche in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="bb37c-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="bb37c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb37c-107">EXAMPLES</span></span>

### <span data-ttu-id="bb37c-108">Esempio 1: Eliminare un collegamento di comunicazione</span><span class="sxs-lookup"><span data-stu-id="bb37c-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="bb37c-109">Questo comando elimina un collegamento di comunicazione tra server denominato Link01 in ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="bb37c-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="bb37c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb37c-110">PARAMETERS</span></span>

### <span data-ttu-id="bb37c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb37c-111">-DefaultProfile</span></span>
<span data-ttu-id="bb37c-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bb37c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb37c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bb37c-113">-Force</span></span>
<span data-ttu-id="bb37c-114">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="bb37c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb37c-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="bb37c-115">-LinkName</span></span>
<span data-ttu-id="bb37c-116">Specifica il nome del collegamento di comunicazione server eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb37c-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bb37c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb37c-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb37c-118">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal *parametro ServerName.*</span><span class="sxs-lookup"><span data-stu-id="bb37c-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="bb37c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb37c-119">-ServerName</span></span>
<span data-ttu-id="bb37c-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="bb37c-120">Specifies the name of a server.</span></span>
<span data-ttu-id="bb37c-121">Questo server contiene il collegamento di comunicazione eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb37c-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bb37c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb37c-122">-Confirm</span></span>
<span data-ttu-id="bb37c-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb37c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb37c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb37c-124">-WhatIf</span></span>
<span data-ttu-id="bb37c-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb37c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb37c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb37c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb37c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb37c-127">CommonParameters</span></span>
<span data-ttu-id="bb37c-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb37c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb37c-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb37c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb37c-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb37c-130">INPUTS</span></span>

### <span data-ttu-id="bb37c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bb37c-131">System.String</span></span>

## <span data-ttu-id="bb37c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb37c-132">OUTPUTS</span></span>

### <span data-ttu-id="bb37c-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="bb37c-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="bb37c-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb37c-134">NOTES</span></span>
* <span data-ttu-id="bb37c-135">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="bb37c-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="bb37c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb37c-136">RELATED LINKS</span></span>

[<span data-ttu-id="bb37c-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bb37c-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="bb37c-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bb37c-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="bb37c-139">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="bb37c-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
