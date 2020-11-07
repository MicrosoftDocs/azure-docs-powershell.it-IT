---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 63bfce9b6f0d6aaa97fede65d8c96ac9079be349
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688214"
---
# <span data-ttu-id="d68ba-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d68ba-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="d68ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d68ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d68ba-103">Elimina un collegamento di comunicazione per le transazioni di database elastiche tra due server.</span><span class="sxs-lookup"><span data-stu-id="d68ba-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d68ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d68ba-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d68ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d68ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d68ba-106">Il cmdlet **Remove-AzureRmSqlServerCommunicationLink** Elimina un collegamento di comunicazione da server a server per le transazioni di database flessibili in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="d68ba-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="d68ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d68ba-107">EXAMPLES</span></span>

### <span data-ttu-id="d68ba-108">Esempio 1: eliminare un collegamento di comunicazione</span><span class="sxs-lookup"><span data-stu-id="d68ba-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="d68ba-109">Questo comando Elimina un collegamento di comunicazione da server a server denominato Link01 in ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="d68ba-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="d68ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d68ba-110">PARAMETERS</span></span>

### <span data-ttu-id="d68ba-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d68ba-111">-Force</span></span>
<span data-ttu-id="d68ba-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d68ba-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d68ba-113">-LinkName</span><span class="sxs-lookup"><span data-stu-id="d68ba-113">-LinkName</span></span>
<span data-ttu-id="d68ba-114">Specifica il nome del collegamento di comunicazione del server eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d68ba-114">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="d68ba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68ba-115">-ResourceGroupName</span></span>
<span data-ttu-id="d68ba-116">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal parametro *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="d68ba-116">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="d68ba-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d68ba-117">-ServerName</span></span>
<span data-ttu-id="d68ba-118">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="d68ba-118">Specifies the name of a server.</span></span>
<span data-ttu-id="d68ba-119">Questo server contiene il collegamento di comunicazione eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d68ba-119">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="d68ba-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d68ba-120">-Confirm</span></span>
<span data-ttu-id="d68ba-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d68ba-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d68ba-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d68ba-122">-WhatIf</span></span>
<span data-ttu-id="d68ba-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d68ba-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d68ba-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d68ba-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d68ba-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68ba-125">-DefaultProfile</span></span>
<span data-ttu-id="d68ba-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d68ba-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68ba-127">CommonParameters</span></span>
<span data-ttu-id="d68ba-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d68ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68ba-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d68ba-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68ba-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d68ba-130">INPUTS</span></span>

## <span data-ttu-id="d68ba-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d68ba-131">OUTPUTS</span></span>

### <span data-ttu-id="d68ba-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d68ba-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="d68ba-133">Note</span><span class="sxs-lookup"><span data-stu-id="d68ba-133">NOTES</span></span>
* <span data-ttu-id="d68ba-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d68ba-134">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d68ba-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d68ba-135">RELATED LINKS</span></span>

[<span data-ttu-id="d68ba-136">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d68ba-136">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="d68ba-137">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d68ba-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="d68ba-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d68ba-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
