---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 333de53ccd3632188100af7f3fcde10e140537c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518547"
---
# <span data-ttu-id="0c15c-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0c15c-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="0c15c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c15c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c15c-103">Aggiunge un certificato di crittografia dati trasparente per l'istanza di SQL Server specificata</span><span class="sxs-lookup"><span data-stu-id="0c15c-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c15c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c15c-104">SYNTAX</span></span>

### <span data-ttu-id="0c15c-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c15c-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c15c-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c15c-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c15c-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c15c-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c15c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c15c-108">DESCRIPTION</span></span>
<span data-ttu-id="0c15c-109">Il Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate aggiunge un certificato di crittografia dati trasparente per l'istanza di SQL Server specificata</span><span class="sxs-lookup"><span data-stu-id="0c15c-109">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="0c15c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c15c-110">EXAMPLES</span></span>

### <span data-ttu-id="0c15c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c15c-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="0c15c-112">Aggiungere un certificato Transparent a un server SQL tramite il nome del gruppo di risorse e il nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="0c15c-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="0c15c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0c15c-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzureRmSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="0c15c-114">Aggiungere un certificato di transparenza ai server tramite server resourceId</span><span class="sxs-lookup"><span data-stu-id="0c15c-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="0c15c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0c15c-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzureRmSqlServer | Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="0c15c-116">Aggiungere un certificato Transparent a tutti i server SQL in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0c15c-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="0c15c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c15c-117">PARAMETERS</span></span>

### <span data-ttu-id="0c15c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c15c-118">-DefaultProfile</span></span>
<span data-ttu-id="0c15c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c15c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c15c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c15c-120">-PassThru</span></span>
<span data-ttu-id="0c15c-121">Per l'esecuzione corretta, restituisce l'oggetto certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="0c15c-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="0c15c-122">-Password</span><span class="sxs-lookup"><span data-stu-id="0c15c-122">-Password</span></span>
<span data-ttu-id="0c15c-123">Password per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="0c15c-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="0c15c-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="0c15c-124">-PrivateBlob</span></span>
<span data-ttu-id="0c15c-125">Il BLOB privato per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="0c15c-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="0c15c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c15c-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c15c-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0c15c-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="0c15c-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0c15c-128">-ServerName</span></span>
<span data-ttu-id="0c15c-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="0c15c-129">The Server Name</span></span>

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

### <span data-ttu-id="0c15c-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="0c15c-130">-SqlServer</span></span>
<span data-ttu-id="0c15c-131">Oggetto di input di SQL Server</span><span class="sxs-lookup"><span data-stu-id="0c15c-131">The sql server input object</span></span>

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

### <span data-ttu-id="0c15c-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="0c15c-132">-SqlServerResourceId</span></span>
<span data-ttu-id="0c15c-133">ID risorsa di SQL Server</span><span class="sxs-lookup"><span data-stu-id="0c15c-133">The sql server resource id</span></span>

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

### <span data-ttu-id="0c15c-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c15c-134">-Confirm</span></span>
<span data-ttu-id="0c15c-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c15c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c15c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c15c-136">-WhatIf</span></span>
<span data-ttu-id="0c15c-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c15c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c15c-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c15c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c15c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c15c-139">CommonParameters</span></span>
<span data-ttu-id="0c15c-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c15c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c15c-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c15c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c15c-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c15c-142">INPUTS</span></span>

### <span data-ttu-id="0c15c-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="0c15c-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="0c15c-144">Parametri: SqlServer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c15c-144">Parameters: SqlServer (ByValue)</span></span>

### <span data-ttu-id="0c15c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0c15c-145">System.String</span></span>

## <span data-ttu-id="0c15c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c15c-146">OUTPUTS</span></span>

### <span data-ttu-id="0c15c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c15c-147">System.Boolean</span></span>

## <span data-ttu-id="0c15c-148">Note</span><span class="sxs-lookup"><span data-stu-id="0c15c-148">NOTES</span></span>

## <span data-ttu-id="0c15c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c15c-149">RELATED LINKS</span></span>
