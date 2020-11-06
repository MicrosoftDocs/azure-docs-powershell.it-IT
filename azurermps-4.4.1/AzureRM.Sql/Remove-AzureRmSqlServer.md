---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 48b1ee50f1ebd0003097500849a6d03dac64c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521953"
---
# <span data-ttu-id="1ed10-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1ed10-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="1ed10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ed10-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed10-103">Rimuove un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed10-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ed10-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed10-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ed10-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed10-106">Il cmdlet **Remove-AzureRmSqlServer** rimuove un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed10-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="1ed10-107">L'operazione di eliminazione è asincrona e può richiedere del tempo, quindi verificare che l'operazione sia terminata prima di eseguire altre operazioni che dipendono dal server che viene completamente eliminato.</span><span class="sxs-lookup"><span data-stu-id="1ed10-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="1ed10-108">Ad esempio, devi creare un nuovo server che usa lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="1ed10-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="1ed10-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ed10-109">EXAMPLES</span></span>

### <span data-ttu-id="1ed10-110">Esempio 1: rimuovere un server</span><span class="sxs-lookup"><span data-stu-id="1ed10-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="1ed10-111">Questo comando rimuove il server di database SQL di Azure denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="1ed10-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="1ed10-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ed10-112">PARAMETERS</span></span>

### <span data-ttu-id="1ed10-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1ed10-113">-Force</span></span>
<span data-ttu-id="1ed10-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1ed10-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ed10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed10-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ed10-116">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="1ed10-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1ed10-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1ed10-117">-ServerName</span></span>
<span data-ttu-id="1ed10-118">Specifica il nome del server da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1ed10-118">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="1ed10-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ed10-119">-Confirm</span></span>
<span data-ttu-id="1ed10-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed10-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed10-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed10-121">-WhatIf</span></span>
<span data-ttu-id="1ed10-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ed10-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed10-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ed10-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed10-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed10-124">-DefaultProfile</span></span>
<span data-ttu-id="1ed10-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed10-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed10-126">CommonParameters</span></span>
<span data-ttu-id="1ed10-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed10-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed10-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ed10-129">INPUTS</span></span>

### <span data-ttu-id="1ed10-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1ed10-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1ed10-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ed10-131">OUTPUTS</span></span>

### <span data-ttu-id="1ed10-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1ed10-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1ed10-133">Note</span><span class="sxs-lookup"><span data-stu-id="1ed10-133">NOTES</span></span>

## <span data-ttu-id="1ed10-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ed10-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ed10-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1ed10-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="1ed10-136">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1ed10-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="1ed10-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1ed10-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="1ed10-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1ed10-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


