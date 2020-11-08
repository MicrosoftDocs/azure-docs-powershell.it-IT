---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023929"
---
# <span data-ttu-id="c002c-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c002c-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="c002c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c002c-102">SYNOPSIS</span></span>
<span data-ttu-id="c002c-103">Crea un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c002c-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="c002c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c002c-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c002c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c002c-105">DESCRIPTION</span></span>
<span data-ttu-id="c002c-106">Il cmdlet **New-AzureSqlDatabaseServer** crea un'istanza del server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c002c-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="c002c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c002c-107">EXAMPLES</span></span>

### <span data-ttu-id="c002c-108">Esempio 1: creare un server</span><span class="sxs-lookup"><span data-stu-id="c002c-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="c002c-109">Questo comando crea un server di database SQL di Azure versione 11.</span><span class="sxs-lookup"><span data-stu-id="c002c-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="c002c-110">Esempio 2: creare un server versione 12</span><span class="sxs-lookup"><span data-stu-id="c002c-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="c002c-111">Questo comando crea un server versione 12.</span><span class="sxs-lookup"><span data-stu-id="c002c-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="c002c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c002c-112">PARAMETERS</span></span>

### <span data-ttu-id="c002c-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="c002c-113">-AdministratorLogin</span></span>
<span data-ttu-id="c002c-114">Specifica il nome dell'account di amministratore per il nuovo server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c002c-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

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

### <span data-ttu-id="c002c-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c002c-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c002c-116">Specifica la password dell'account di amministratore per il server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c002c-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="c002c-117">Devi specificare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="c002c-117">You must specify a strong password.</span></span>
<span data-ttu-id="c002c-118">Per altre informazioni, Vedi [password complesse](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) nella rete Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="c002c-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="c002c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c002c-119">-Force</span></span>
<span data-ttu-id="c002c-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c002c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c002c-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c002c-121">-Location</span></span>
<span data-ttu-id="c002c-122">Specifica la posizione del centro dati in cui questo cmdlet crea il server.</span><span class="sxs-lookup"><span data-stu-id="c002c-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="c002c-123">Per altre informazioni, vedere [aree di Azure](https://azure.microsoft.com/regions/) ( https://azure.microsoft.com/regions/#services) nella raccolta di Azure.</span><span class="sxs-lookup"><span data-stu-id="c002c-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

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

### <span data-ttu-id="c002c-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="c002c-124">-Profile</span></span>
<span data-ttu-id="c002c-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c002c-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c002c-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c002c-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c002c-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="c002c-127">-Version</span></span>
<span data-ttu-id="c002c-128">Specifica la versione del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="c002c-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="c002c-129">I valori validi sono: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="c002c-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c002c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c002c-130">-Confirm</span></span>
<span data-ttu-id="c002c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c002c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c002c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c002c-132">-WhatIf</span></span>
<span data-ttu-id="c002c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c002c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c002c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c002c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c002c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c002c-135">CommonParameters</span></span>
<span data-ttu-id="c002c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c002c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c002c-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c002c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c002c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c002c-138">INPUTS</span></span>

## <span data-ttu-id="c002c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c002c-139">OUTPUTS</span></span>

### <span data-ttu-id="c002c-140">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="c002c-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="c002c-141">Note</span><span class="sxs-lookup"><span data-stu-id="c002c-141">NOTES</span></span>

## <span data-ttu-id="c002c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c002c-142">RELATED LINKS</span></span>

[<span data-ttu-id="c002c-143">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="c002c-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c002c-144">Creare un server</span><span class="sxs-lookup"><span data-stu-id="c002c-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="c002c-145">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="c002c-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c002c-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c002c-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c002c-147">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c002c-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c002c-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c002c-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


