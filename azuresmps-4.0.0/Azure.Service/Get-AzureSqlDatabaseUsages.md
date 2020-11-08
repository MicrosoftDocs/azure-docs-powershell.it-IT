---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030025"
---
# <span data-ttu-id="e1dda-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="e1dda-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="e1dda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1dda-102">SYNOPSIS</span></span>
<span data-ttu-id="e1dda-103">Ottiene il limite di dimensioni e dimensioni di un database SQL.</span><span class="sxs-lookup"><span data-stu-id="e1dda-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="e1dda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1dda-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1dda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1dda-105">DESCRIPTION</span></span>
<span data-ttu-id="e1dda-106">Il cmdlet **Get-AzureSqlDatabaseUsages** ottiene il limite di dimensioni e dimensioni correnti di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dda-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="e1dda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1dda-107">EXAMPLES</span></span>

### <span data-ttu-id="e1dda-108">Esempio 1: ottenere le informazioni sull'utilizzo per un database SQL</span><span class="sxs-lookup"><span data-stu-id="e1dda-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="e1dda-109">Questo comando consente di ottenere le informazioni sul limite di dimensioni e dimensioni per il database SQL denominato Database01 in Server01.</span><span class="sxs-lookup"><span data-stu-id="e1dda-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="e1dda-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1dda-110">PARAMETERS</span></span>

### <span data-ttu-id="e1dda-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1dda-111">-DatabaseName</span></span>
<span data-ttu-id="e1dda-112">Specifica il nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dda-112">Specifies the name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e1dda-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="e1dda-113">-Profile</span></span>
<span data-ttu-id="e1dda-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1dda-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1dda-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e1dda-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1dda-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e1dda-116">-ServerName</span></span>
<span data-ttu-id="e1dda-117">Specifica il nome del server che ospita il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dda-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e1dda-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1dda-118">CommonParameters</span></span>
<span data-ttu-id="e1dda-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1dda-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1dda-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1dda-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1dda-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1dda-121">INPUTS</span></span>

## <span data-ttu-id="e1dda-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1dda-122">OUTPUTS</span></span>

## <span data-ttu-id="e1dda-123">Note</span><span class="sxs-lookup"><span data-stu-id="e1dda-123">NOTES</span></span>

## <span data-ttu-id="e1dda-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1dda-124">RELATED LINKS</span></span>

