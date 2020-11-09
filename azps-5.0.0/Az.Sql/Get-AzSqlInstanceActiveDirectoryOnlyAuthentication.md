---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300114"
---
# <span data-ttu-id="caccd-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="caccd-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="caccd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="caccd-102">SYNOPSIS</span></span>
<span data-ttu-id="caccd-103">Ottiene l'autenticazione di Azure AD solo per un'istanza specifica gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="caccd-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="caccd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="caccd-104">SYNTAX</span></span>

### <span data-ttu-id="caccd-105">UseResourceGroupAndInstanceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="caccd-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caccd-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caccd-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caccd-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="caccd-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caccd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caccd-108">DESCRIPTION</span></span>
<span data-ttu-id="caccd-109">Il cmdlet **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** ottiene solo Azure Active Directory (Azure ad) solo il requisito di autenticazione per un'istanza gestita di AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="caccd-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="caccd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="caccd-110">EXAMPLES</span></span>

### <span data-ttu-id="caccd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="caccd-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="caccd-112">Questo comando ottiene il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un'istanza gestita AzureSQL denominata ManagedInstance01 associata a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="caccd-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="caccd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="caccd-113">PARAMETERS</span></span>

### <span data-ttu-id="caccd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caccd-114">-DefaultProfile</span></span>
<span data-ttu-id="caccd-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="caccd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caccd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caccd-116">-InputObject</span></span>
<span data-ttu-id="caccd-117">Oggetto istanza gestito da usare.</span><span class="sxs-lookup"><span data-stu-id="caccd-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caccd-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="caccd-118">-InstanceName</span></span>
<span data-ttu-id="caccd-119">Nome dell'istanza gestita di Azure SQL in cui è attiva solo l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="caccd-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caccd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caccd-120">-ResourceGroupName</span></span>
<span data-ttu-id="caccd-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="caccd-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caccd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caccd-122">-ResourceId</span></span>
<span data-ttu-id="caccd-123">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="caccd-123">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caccd-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="caccd-124">-Confirm</span></span>
<span data-ttu-id="caccd-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caccd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caccd-126">-WhatIf</span></span>
<span data-ttu-id="caccd-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="caccd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caccd-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="caccd-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caccd-129">CommonParameters</span></span>
<span data-ttu-id="caccd-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caccd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caccd-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="caccd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caccd-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="caccd-132">INPUTS</span></span>

### <span data-ttu-id="caccd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="caccd-133">System.String</span></span>

## <span data-ttu-id="caccd-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="caccd-134">OUTPUTS</span></span>

### <span data-ttu-id="caccd-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="caccd-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="caccd-136">Note</span><span class="sxs-lookup"><span data-stu-id="caccd-136">NOTES</span></span>

## <span data-ttu-id="caccd-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="caccd-137">RELATED LINKS</span></span>

[<span data-ttu-id="caccd-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="caccd-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="caccd-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="caccd-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="caccd-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="caccd-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="caccd-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="caccd-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

