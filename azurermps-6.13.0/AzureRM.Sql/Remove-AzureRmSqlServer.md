---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: a6afa65eaf77cbc30ba63485112c52114d6ddded
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687250"
---
# <span data-ttu-id="d83d1-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83d1-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="d83d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d83d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d83d1-103">Rimuove un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d83d1-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d83d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d83d1-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d83d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d83d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d83d1-106">Il cmdlet **Remove-AzureRmSqlServer** rimuove un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d83d1-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="d83d1-107">L'operazione di eliminazione è asincrona e può richiedere del tempo, quindi verificare che l'operazione sia terminata prima di eseguire altre operazioni che dipendono dal server che viene completamente eliminato.</span><span class="sxs-lookup"><span data-stu-id="d83d1-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="d83d1-108">Ad esempio, devi creare un nuovo server che usa lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="d83d1-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="d83d1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d83d1-109">EXAMPLES</span></span>

### <span data-ttu-id="d83d1-110">Esempio 1: rimuovere un server</span><span class="sxs-lookup"><span data-stu-id="d83d1-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="d83d1-111">Questo comando rimuove il server di database SQL di Azure denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="d83d1-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="d83d1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d83d1-112">PARAMETERS</span></span>

### <span data-ttu-id="d83d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83d1-113">-DefaultProfile</span></span>
<span data-ttu-id="d83d1-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d83d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d83d1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d83d1-115">-Force</span></span>
<span data-ttu-id="d83d1-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d83d1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d83d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="d83d1-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="d83d1-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d83d1-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d83d1-119">-ServerName</span></span>
<span data-ttu-id="d83d1-120">Specifica il nome del server da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d83d1-120">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="d83d1-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d83d1-121">-Confirm</span></span>
<span data-ttu-id="d83d1-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d83d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d83d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d83d1-123">-WhatIf</span></span>
<span data-ttu-id="d83d1-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d83d1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d83d1-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d83d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d83d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83d1-126">CommonParameters</span></span>
<span data-ttu-id="d83d1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83d1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83d1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d83d1-129">INPUTS</span></span>

### <span data-ttu-id="d83d1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d83d1-130">System.String</span></span>

## <span data-ttu-id="d83d1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d83d1-131">OUTPUTS</span></span>

### <span data-ttu-id="d83d1-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d83d1-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="d83d1-133">Note</span><span class="sxs-lookup"><span data-stu-id="d83d1-133">NOTES</span></span>

## <span data-ttu-id="d83d1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d83d1-134">RELATED LINKS</span></span>

[<span data-ttu-id="d83d1-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83d1-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="d83d1-136">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83d1-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="d83d1-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d83d1-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="d83d1-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d83d1-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


