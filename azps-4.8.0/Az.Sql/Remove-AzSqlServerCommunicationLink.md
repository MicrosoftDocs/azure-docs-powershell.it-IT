---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188762"
---
# <span data-ttu-id="9fc53-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="9fc53-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="9fc53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fc53-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc53-103">Elimina un collegamento di comunicazione per le transazioni di database elastiche tra due server.</span><span class="sxs-lookup"><span data-stu-id="9fc53-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="9fc53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fc53-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc53-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fc53-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc53-106">Il cmdlet **Remove-AzSqlServerCommunicationLink** Elimina un collegamento di comunicazione da server a server per le transazioni di database flessibili in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="9fc53-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="9fc53-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fc53-107">EXAMPLES</span></span>

### <span data-ttu-id="9fc53-108">Esempio 1: eliminare un collegamento di comunicazione</span><span class="sxs-lookup"><span data-stu-id="9fc53-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="9fc53-109">Questo comando Elimina un collegamento di comunicazione da server a server denominato Link01 in ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="9fc53-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="9fc53-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fc53-110">PARAMETERS</span></span>

### <span data-ttu-id="9fc53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc53-111">-DefaultProfile</span></span>
<span data-ttu-id="9fc53-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9fc53-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fc53-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9fc53-113">-Force</span></span>
<span data-ttu-id="9fc53-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9fc53-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9fc53-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="9fc53-115">-LinkName</span></span>
<span data-ttu-id="9fc53-116">Specifica il nome del collegamento di comunicazione del server eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc53-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="9fc53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc53-117">-ResourceGroupName</span></span>
<span data-ttu-id="9fc53-118">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal parametro *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="9fc53-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="9fc53-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9fc53-119">-ServerName</span></span>
<span data-ttu-id="9fc53-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="9fc53-120">Specifies the name of a server.</span></span>
<span data-ttu-id="9fc53-121">Questo server contiene il collegamento di comunicazione eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc53-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="9fc53-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9fc53-122">-Confirm</span></span>
<span data-ttu-id="9fc53-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc53-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fc53-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fc53-124">-WhatIf</span></span>
<span data-ttu-id="9fc53-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fc53-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fc53-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fc53-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fc53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc53-127">CommonParameters</span></span>
<span data-ttu-id="9fc53-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc53-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fc53-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc53-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fc53-130">INPUTS</span></span>

### <span data-ttu-id="9fc53-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9fc53-131">System.String</span></span>

## <span data-ttu-id="9fc53-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fc53-132">OUTPUTS</span></span>

### <span data-ttu-id="9fc53-133">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="9fc53-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="9fc53-134">Note</span><span class="sxs-lookup"><span data-stu-id="9fc53-134">NOTES</span></span>
* <span data-ttu-id="9fc53-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="9fc53-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="9fc53-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fc53-136">RELATED LINKS</span></span>

[<span data-ttu-id="9fc53-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="9fc53-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="9fc53-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="9fc53-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="9fc53-139">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9fc53-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
