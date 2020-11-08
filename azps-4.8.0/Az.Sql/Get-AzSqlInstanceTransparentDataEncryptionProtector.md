---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191879"
---
# <span data-ttu-id="ebf5a-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ebf5a-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="ebf5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ebf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf5a-103">Ottiene la protezione di crittografia dati trasparente (Transparent Data Encryption) per un'istanza gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="ebf5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebf5a-104">SYNTAX</span></span>

### <span data-ttu-id="ebf5a-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ebf5a-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf5a-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebf5a-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf5a-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebf5a-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf5a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebf5a-108">DESCRIPTION</span></span>
<span data-ttu-id="ebf5a-109">Il cmdlet Get-AzSqlInstanceTransparentDataEncryptionProtector ottiene la protezione di Transparent per l'istanza di SQL Managed specificata.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="ebf5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebf5a-110">EXAMPLES</span></span>

### <span data-ttu-id="ebf5a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ebf5a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="ebf5a-112">Questo comando consente di ottenere la protezione di Transparent per l'istanza gestita denominata ContosoManagedInstanceName nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ebf5a-113">Esempio 2: uso dell'oggetto istanza gestito</span><span class="sxs-lookup"><span data-stu-id="ebf5a-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="ebf5a-114">Questo comando consente di ottenere la protezione di Transparent per l'istanza gestita denominata ContosoManagedInstanceName nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ebf5a-115">Esempio 3: uso dell'ID risorsa istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ebf5a-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="ebf5a-116">Questo comando consente di ottenere la protezione di Transparent per l'istanza gestita denominata ContosoManagedInstanceName nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ebf5a-117">Esempio 4: utilizzo di piping</span><span class="sxs-lookup"><span data-stu-id="ebf5a-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="ebf5a-118">Questo comando consente di ottenere la protezione di Transparent per l'istanza gestita denominata ContosoManagedInstanceName nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="ebf5a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ebf5a-119">PARAMETERS</span></span>

### <span data-ttu-id="ebf5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf5a-120">-DefaultProfile</span></span>
<span data-ttu-id="ebf5a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebf5a-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="ebf5a-122">-Instance</span></span>
<span data-ttu-id="ebf5a-123">Oggetto di input dell'istanza</span><span class="sxs-lookup"><span data-stu-id="ebf5a-123">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf5a-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ebf5a-124">-InstanceName</span></span>
<span data-ttu-id="ebf5a-125">Nome dell'istanza</span><span class="sxs-lookup"><span data-stu-id="ebf5a-125">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf5a-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf5a-126">-InstanceResourceId</span></span>
<span data-ttu-id="ebf5a-127">ID risorsa istanza</span><span class="sxs-lookup"><span data-stu-id="ebf5a-127">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf5a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf5a-128">-ResourceGroupName</span></span>
<span data-ttu-id="ebf5a-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ebf5a-129">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf5a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ebf5a-130">-Confirm</span></span>
<span data-ttu-id="ebf5a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf5a-132">-WhatIf</span></span>
<span data-ttu-id="ebf5a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebf5a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf5a-135">CommonParameters</span></span>
<span data-ttu-id="ebf5a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf5a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebf5a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf5a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ebf5a-138">INPUTS</span></span>

### <span data-ttu-id="ebf5a-139">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ebf5a-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="ebf5a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf5a-140">System.String</span></span>

## <span data-ttu-id="ebf5a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebf5a-141">OUTPUTS</span></span>

### <span data-ttu-id="ebf5a-142">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="ebf5a-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="ebf5a-143">Note</span><span class="sxs-lookup"><span data-stu-id="ebf5a-143">NOTES</span></span>

## <span data-ttu-id="ebf5a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebf5a-144">RELATED LINKS</span></span>