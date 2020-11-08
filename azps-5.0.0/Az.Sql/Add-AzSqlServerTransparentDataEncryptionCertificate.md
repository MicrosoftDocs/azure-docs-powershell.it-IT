---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193162"
---
# <span data-ttu-id="3cf10-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="3cf10-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="3cf10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3cf10-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf10-103">Aggiunge un certificato di crittografia dati trasparente per l'istanza di SQL Server specificata</span><span class="sxs-lookup"><span data-stu-id="3cf10-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="3cf10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cf10-104">SYNTAX</span></span>

### <span data-ttu-id="3cf10-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cf10-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf10-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf10-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf10-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf10-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf10-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cf10-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf10-109">Il Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate aggiunge un certificato di crittografia dati trasparente per l'istanza di SQL Server specificata</span><span class="sxs-lookup"><span data-stu-id="3cf10-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="3cf10-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cf10-110">EXAMPLES</span></span>

### <span data-ttu-id="3cf10-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3cf10-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="3cf10-112">Aggiungere un certificato Transparent a un server SQL tramite il nome del gruppo di risorse e il nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="3cf10-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="3cf10-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3cf10-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="3cf10-114">Aggiungere un certificato di transparenza ai server tramite server resourceId</span><span class="sxs-lookup"><span data-stu-id="3cf10-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="3cf10-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3cf10-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="3cf10-116">Aggiungere un certificato Transparent a tutti i server SQL in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3cf10-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="3cf10-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3cf10-117">PARAMETERS</span></span>

### <span data-ttu-id="3cf10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf10-118">-DefaultProfile</span></span>
<span data-ttu-id="3cf10-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf10-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf10-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cf10-120">-PassThru</span></span>
<span data-ttu-id="3cf10-121">Per l'esecuzione corretta, restituisce l'oggetto certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="3cf10-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="3cf10-122">-Password</span><span class="sxs-lookup"><span data-stu-id="3cf10-122">-Password</span></span>
<span data-ttu-id="3cf10-123">Password per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="3cf10-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf10-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="3cf10-124">-PrivateBlob</span></span>
<span data-ttu-id="3cf10-125">Il BLOB privato per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="3cf10-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf10-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf10-126">-ResourceGroupName</span></span>
<span data-ttu-id="3cf10-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3cf10-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf10-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="3cf10-128">-ServerName</span></span>
<span data-ttu-id="3cf10-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="3cf10-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf10-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="3cf10-130">-SqlServer</span></span>
<span data-ttu-id="3cf10-131">Oggetto di input di SQL Server</span><span class="sxs-lookup"><span data-stu-id="3cf10-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf10-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf10-132">-SqlServerResourceId</span></span>
<span data-ttu-id="3cf10-133">ID risorsa di SQL Server</span><span class="sxs-lookup"><span data-stu-id="3cf10-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf10-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3cf10-134">-Confirm</span></span>
<span data-ttu-id="3cf10-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf10-136">-WhatIf</span></span>
<span data-ttu-id="3cf10-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cf10-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf10-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cf10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf10-139">CommonParameters</span></span>
<span data-ttu-id="3cf10-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf10-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cf10-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf10-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3cf10-142">INPUTS</span></span>

### <span data-ttu-id="3cf10-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3cf10-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="3cf10-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf10-144">System.String</span></span>

## <span data-ttu-id="3cf10-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cf10-145">OUTPUTS</span></span>

### <span data-ttu-id="3cf10-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cf10-146">System.Boolean</span></span>

## <span data-ttu-id="3cf10-147">Note</span><span class="sxs-lookup"><span data-stu-id="3cf10-147">NOTES</span></span>

## <span data-ttu-id="3cf10-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cf10-148">RELATED LINKS</span></span>