---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 4f9abf17be9b90cb4650c6f38748702dc0955b9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514072"
---
# <span data-ttu-id="845e7-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="845e7-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="845e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="845e7-102">SYNOPSIS</span></span>
<span data-ttu-id="845e7-103">Elimina un collegamento di comunicazione per le transazioni di database elastiche tra due server.</span><span class="sxs-lookup"><span data-stu-id="845e7-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="845e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="845e7-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="845e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="845e7-105">DESCRIPTION</span></span>
<span data-ttu-id="845e7-106">Il cmdlet **Remove-AzureRmSqlServerCommunicationLink** Elimina un collegamento di comunicazione da server a server per le transazioni di database flessibili in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="845e7-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="845e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="845e7-107">EXAMPLES</span></span>

### <span data-ttu-id="845e7-108">Esempio 1: eliminare un collegamento di comunicazione</span><span class="sxs-lookup"><span data-stu-id="845e7-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="845e7-109">Questo comando Elimina un collegamento di comunicazione da server a server denominato Link01 in ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="845e7-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="845e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="845e7-110">PARAMETERS</span></span>

### <span data-ttu-id="845e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845e7-111">-DefaultProfile</span></span>
<span data-ttu-id="845e7-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="845e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="845e7-113">-Force</span></span>
<span data-ttu-id="845e7-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="845e7-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845e7-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="845e7-115">-LinkName</span></span>
<span data-ttu-id="845e7-116">Specifica il nome del collegamento di comunicazione del server eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="845e7-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="845e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="845e7-118">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal parametro *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="845e7-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845e7-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="845e7-119">-ServerName</span></span>
<span data-ttu-id="845e7-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="845e7-120">Specifies the name of a server.</span></span>
<span data-ttu-id="845e7-121">Questo server contiene il collegamento di comunicazione eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="845e7-121">This server contains the communication link that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845e7-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="845e7-122">-Confirm</span></span>
<span data-ttu-id="845e7-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="845e7-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845e7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845e7-124">-WhatIf</span></span>
<span data-ttu-id="845e7-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="845e7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="845e7-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="845e7-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845e7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845e7-127">CommonParameters</span></span>
<span data-ttu-id="845e7-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="845e7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845e7-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="845e7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845e7-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="845e7-130">INPUTS</span></span>

### <span data-ttu-id="845e7-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="845e7-131">None</span></span>
<span data-ttu-id="845e7-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="845e7-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="845e7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="845e7-133">OUTPUTS</span></span>

### <span data-ttu-id="845e7-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="845e7-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="845e7-135">Note</span><span class="sxs-lookup"><span data-stu-id="845e7-135">NOTES</span></span>
* <span data-ttu-id="845e7-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="845e7-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="845e7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="845e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="845e7-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="845e7-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="845e7-139">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="845e7-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="845e7-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="845e7-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
