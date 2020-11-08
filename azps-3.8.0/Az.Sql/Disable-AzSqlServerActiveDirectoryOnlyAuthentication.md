---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019975"
---
# <span data-ttu-id="0d160-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0d160-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="0d160-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d160-102">SYNOPSIS</span></span>
<span data-ttu-id="0d160-103">Disabilita l'autenticazione di Azure AD solo per un determinato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0d160-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="0d160-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d160-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d160-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d160-105">DESCRIPTION</span></span>
<span data-ttu-id="0d160-106">Il cmdlet **Disable-AzSqlServerActiveDirectoryOnlyAuthentication Disabilita** il requisito di autenticazione di Azure Active Directory (Azure ad) solo per un server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="0d160-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="0d160-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d160-107">EXAMPLES</span></span>

### <span data-ttu-id="0d160-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d160-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="0d160-109">Questo comando Disabilita Azure Active Directory (Azure AD) solo il requisito di autenticazione per un server AzureSQL denominato Server01 associato a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0d160-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0d160-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d160-110">PARAMETERS</span></span>

### <span data-ttu-id="0d160-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d160-111">-DefaultProfile</span></span>
<span data-ttu-id="0d160-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d160-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d160-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d160-113">-ResourceGroupName</span></span>
<span data-ttu-id="0d160-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d160-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d160-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0d160-115">-ServerName</span></span>
<span data-ttu-id="0d160-116">Nome di Azure SQL Server in cui è presente l'amministratore di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0d160-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

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

### <span data-ttu-id="0d160-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d160-117">-Confirm</span></span>
<span data-ttu-id="0d160-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d160-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d160-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d160-119">-WhatIf</span></span>
<span data-ttu-id="0d160-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d160-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d160-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d160-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d160-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d160-122">CommonParameters</span></span>
<span data-ttu-id="0d160-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d160-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d160-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d160-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d160-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d160-125">INPUTS</span></span>

### <span data-ttu-id="0d160-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0d160-126">System.String</span></span>

## <span data-ttu-id="0d160-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d160-127">OUTPUTS</span></span>

### <span data-ttu-id="0d160-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="0d160-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="0d160-129">Note</span><span class="sxs-lookup"><span data-stu-id="0d160-129">NOTES</span></span>

## <span data-ttu-id="0d160-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d160-130">RELATED LINKS</span></span>

[<span data-ttu-id="0d160-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0d160-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0d160-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0d160-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0d160-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0d160-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="0d160-134">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0d160-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
