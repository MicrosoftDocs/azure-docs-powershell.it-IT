---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475667"
---
# <span data-ttu-id="23fb7-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="23fb7-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="23fb7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="23fb7-103">Ottiene informazioni su un amministratore di Azure AD per l'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="23fb7-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="23fb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23fb7-104">SYNTAX</span></span>

### <span data-ttu-id="23fb7-105">UseResourceGroupAndInstanceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23fb7-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23fb7-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23fb7-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23fb7-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23fb7-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23fb7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23fb7-108">DESCRIPTION</span></span>
<span data-ttu-id="23fb7-109">Il cmdlet **Get-AzSqlInstanceActiveDirectoryAdministrator** ottiene le informazioni su un amministratore di Azure Active Directory (Azure ad) per un'istanza gestita di AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="23fb7-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="23fb7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23fb7-110">EXAMPLES</span></span>

### <span data-ttu-id="23fb7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23fb7-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="23fb7-112">Questo comando consente di ottenere informazioni su un amministratore di Azure AD per un'istanza gestita denominata ManagedInstance01 associata a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="23fb7-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="23fb7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="23fb7-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="23fb7-114">Questo comando consente di ottenere informazioni su un amministratore di Azure AD da un oggetto istanza gestito.</span><span class="sxs-lookup"><span data-stu-id="23fb7-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="23fb7-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="23fb7-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="23fb7-116">Questo comando consente di ottenere informazioni su un amministratore di Azure AD usando l'identificatore delle risorse di istanza gestito.</span><span class="sxs-lookup"><span data-stu-id="23fb7-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="23fb7-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23fb7-117">PARAMETERS</span></span>

### <span data-ttu-id="23fb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fb7-118">-DefaultProfile</span></span>
<span data-ttu-id="23fb7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23fb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23fb7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23fb7-120">-InputObject</span></span>
<span data-ttu-id="23fb7-121">Oggetto istanza gestito da usare.</span><span class="sxs-lookup"><span data-stu-id="23fb7-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="23fb7-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="23fb7-122">-InstanceName</span></span>
<span data-ttu-id="23fb7-123">Nome dell'istanza gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="23fb7-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="23fb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23fb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="23fb7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23fb7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="23fb7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23fb7-126">-ResourceId</span></span>
<span data-ttu-id="23fb7-127">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="23fb7-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="23fb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fb7-128">CommonParameters</span></span>
<span data-ttu-id="23fb7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23fb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fb7-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23fb7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fb7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23fb7-131">INPUTS</span></span>

### <span data-ttu-id="23fb7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23fb7-132">System.String</span></span>

## <span data-ttu-id="23fb7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23fb7-133">OUTPUTS</span></span>

### <span data-ttu-id="23fb7-134">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="23fb7-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="23fb7-135">Note</span><span class="sxs-lookup"><span data-stu-id="23fb7-135">NOTES</span></span>

## <span data-ttu-id="23fb7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23fb7-136">RELATED LINKS</span></span>

[<span data-ttu-id="23fb7-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="23fb7-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="23fb7-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="23fb7-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
