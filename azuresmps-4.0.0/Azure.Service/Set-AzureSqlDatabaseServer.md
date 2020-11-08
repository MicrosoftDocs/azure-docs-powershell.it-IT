---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023822"
---
# <span data-ttu-id="3ad76-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="3ad76-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="3ad76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ad76-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad76-103">Modifica le proprietà di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad76-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="3ad76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ad76-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ad76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ad76-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad76-106">Il cmdlet **set-AzureSqlDatabaseServer** modifica le proprietà dell'istanza specificata del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad76-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="3ad76-107">Nella versione corrente è possibile aggiornare solo la password dell'account di amministratore per un server.</span><span class="sxs-lookup"><span data-stu-id="3ad76-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="3ad76-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ad76-108">EXAMPLES</span></span>

### <span data-ttu-id="3ad76-109">Esempio 1: cambiare la password di un server</span><span class="sxs-lookup"><span data-stu-id="3ad76-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="3ad76-110">Questo comando modifica la password dell'account di amministratore per il server di database SQL di Azure denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="3ad76-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="3ad76-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ad76-111">PARAMETERS</span></span>

### <span data-ttu-id="3ad76-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="3ad76-112">-AdminPassword</span></span>
<span data-ttu-id="3ad76-113">Specifica la password dell'account di amministratore per il server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad76-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="3ad76-114">Devi specificare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="3ad76-114">You must specify a strong password.</span></span>
<span data-ttu-id="3ad76-115">Per altre informazioni, Vedi [password complesse](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) nella rete Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="3ad76-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad76-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3ad76-116">-Force</span></span>
<span data-ttu-id="3ad76-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3ad76-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ad76-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="3ad76-118">-Profile</span></span>
<span data-ttu-id="3ad76-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ad76-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ad76-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3ad76-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ad76-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="3ad76-121">-ServerName</span></span>
<span data-ttu-id="3ad76-122">Specifica il nome del server che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3ad76-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="3ad76-123">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="3ad76-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad76-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ad76-124">-Confirm</span></span>
<span data-ttu-id="3ad76-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ad76-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad76-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad76-126">-WhatIf</span></span>
<span data-ttu-id="3ad76-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ad76-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad76-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ad76-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ad76-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad76-129">CommonParameters</span></span>
<span data-ttu-id="3ad76-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad76-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad76-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad76-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad76-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ad76-132">INPUTS</span></span>

### <span data-ttu-id="3ad76-133">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="3ad76-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="3ad76-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ad76-134">OUTPUTS</span></span>

## <span data-ttu-id="3ad76-135">Note</span><span class="sxs-lookup"><span data-stu-id="3ad76-135">NOTES</span></span>

## <span data-ttu-id="3ad76-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ad76-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ad76-137">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="3ad76-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="3ad76-138">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="3ad76-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="3ad76-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="3ad76-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="3ad76-140">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="3ad76-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="3ad76-141">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="3ad76-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


