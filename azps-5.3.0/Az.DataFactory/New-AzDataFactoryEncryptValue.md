---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477132"
---
# <span data-ttu-id="862c2-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="862c2-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="862c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="862c2-102">SYNOPSIS</span></span>
<span data-ttu-id="862c2-103">Crittografa i dati riservati.</span><span class="sxs-lookup"><span data-stu-id="862c2-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="862c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="862c2-104">SYNTAX</span></span>

### <span data-ttu-id="862c2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="862c2-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="862c2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="862c2-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="862c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="862c2-107">DESCRIPTION</span></span>
<span data-ttu-id="862c2-108">Il cmdlet **New-AzDataFactoryEncryptValue** crittografa i dati riservati, ad esempio una password o una stringa di connessione di Microsoft SQL Server, e restituisce un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="862c2-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="862c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="862c2-109">EXAMPLES</span></span>

### <span data-ttu-id="862c2-110">Esempio 1: crittografare una stringa di connessione non ODBC</span><span class="sxs-lookup"><span data-stu-id="862c2-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="862c2-111">Il primo comando usa il cmdlet ConvertTo-SecureString per convertire la stringa di connessione specificata in un oggetto **SecureString** e quindi archivia tale oggetto nella variabile $value.</span><span class="sxs-lookup"><span data-stu-id="862c2-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="862c2-112">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="862c2-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="862c2-113">Valori consentiti: stringa di connessione SQL Server o Oracle.</span><span class="sxs-lookup"><span data-stu-id="862c2-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="862c2-114">Il secondo comando crea un valore crittografato per l'oggetto archiviato in $Value per la data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificati.</span><span class="sxs-lookup"><span data-stu-id="862c2-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="862c2-115">Esempio 2: crittografare una stringa di connessione non ODBC che usa l'autenticazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="862c2-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="862c2-116">Il primo comando utilizza **ConvertTo-SecureString** per convertire la stringa di connessione specificata in un oggetto String sicuro e quindi archivia tale oggetto nella variabile $value.</span><span class="sxs-lookup"><span data-stu-id="862c2-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="862c2-117">Il secondo comando usa il cmdlet Get-Credential per raccogliere l'autenticazione di Windows (nome utente e password) e quindi archivia l'oggetto **PSCredential** nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="862c2-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="862c2-118">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="862c2-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="862c2-119">Il terzo comando crea un valore crittografato per l'oggetto archiviato in $Value e $Credential per la data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificati.</span><span class="sxs-lookup"><span data-stu-id="862c2-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="862c2-120">Esempio 3: crittografare il nome del server e le credenziali per il servizio collegato al file System</span><span class="sxs-lookup"><span data-stu-id="862c2-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="862c2-121">Il primo comando utilizza **ConvertTo-SecureString** per convertire la stringa specificata in una stringa sicura e quindi archivia tale oggetto nella variabile $value.</span><span class="sxs-lookup"><span data-stu-id="862c2-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="862c2-122">Il secondo comando USA **Get-Credential** per raccogliere l'autenticazione di Windows (nome utente e password) e quindi archivia l'oggetto **PSCredential** nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="862c2-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="862c2-123">Il terzo comando crea un valore crittografato per l'oggetto archiviato in $Value e $Credential per la data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificati.</span><span class="sxs-lookup"><span data-stu-id="862c2-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="862c2-124">Esempio 4: crittografare le credenziali per il servizio collegato HDFS</span><span class="sxs-lookup"><span data-stu-id="862c2-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="862c2-125">Il comando **ConvertTo-SecureString** converte la stringa specificata in una stringa sicura.</span><span class="sxs-lookup"><span data-stu-id="862c2-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="862c2-126">Il comando **New-Object** crea un oggetto PSCredential usando le stringhe di nome utente e password sicure.</span><span class="sxs-lookup"><span data-stu-id="862c2-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="862c2-127">Puoi invece usare il comando **Get-Credential** per raccogliere l'autenticazione di Windows (nome utente e password) e quindi archiviare l'oggetto **PSCredential** restituito nella variabile $Credential, come illustrato negli esempi precedenti.</span><span class="sxs-lookup"><span data-stu-id="862c2-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="862c2-128">Il comando **New-AzDataFactoryEncryptValue** crea un valore crittografato per l'oggetto archiviato in $Credential per la data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificati.</span><span class="sxs-lookup"><span data-stu-id="862c2-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="862c2-129">Esempio 5: crittografare le credenziali per il servizio collegato ODBC</span><span class="sxs-lookup"><span data-stu-id="862c2-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="862c2-130">Il comando **ConvertTo-SecureString** converte la stringa specificata in una stringa sicura.</span><span class="sxs-lookup"><span data-stu-id="862c2-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="862c2-131">Il comando **New-AzDataFactoryEncryptValue** crea un valore crittografato per l'oggetto archiviato in $value per la data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificati.</span><span class="sxs-lookup"><span data-stu-id="862c2-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="862c2-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="862c2-132">PARAMETERS</span></span>

### <span data-ttu-id="862c2-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="862c2-133">-AuthenticationType</span></span>
<span data-ttu-id="862c2-134">Specifica il tipo di autenticazione da usare per la connessione all'origine dati.</span><span class="sxs-lookup"><span data-stu-id="862c2-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="862c2-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="862c2-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="862c2-136">Windows</span><span class="sxs-lookup"><span data-stu-id="862c2-136">Windows</span></span>
- <span data-ttu-id="862c2-137">Base</span><span class="sxs-lookup"><span data-stu-id="862c2-137">Basic</span></span>
- <span data-ttu-id="862c2-138">Anonimo.</span><span class="sxs-lookup"><span data-stu-id="862c2-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-139">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="862c2-139">-Credential</span></span>
<span data-ttu-id="862c2-140">Specifica le credenziali di autenticazione di Windows (nome utente e password) da usare.</span><span class="sxs-lookup"><span data-stu-id="862c2-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="862c2-141">Questo cmdlet crittografa i dati delle credenziali specificati qui.</span><span class="sxs-lookup"><span data-stu-id="862c2-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-142">-Database</span><span class="sxs-lookup"><span data-stu-id="862c2-142">-Database</span></span>
<span data-ttu-id="862c2-143">Specifica il nome del database del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="862c2-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="862c2-144">-DataFactory</span></span>
<span data-ttu-id="862c2-145">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="862c2-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="862c2-146">Questo cmdlet crittografa i dati per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="862c2-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-147">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="862c2-147">-DataFactoryName</span></span>
<span data-ttu-id="862c2-148">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="862c2-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="862c2-149">Questo cmdlet crittografa i dati per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="862c2-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862c2-150">-DefaultProfile</span></span>
<span data-ttu-id="862c2-151">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="862c2-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="862c2-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="862c2-152">-GatewayName</span></span>
<span data-ttu-id="862c2-153">Specifica il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="862c2-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="862c2-154">Questo cmdlet crittografa i dati per il gateway specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="862c2-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="862c2-155">-NonCredentialValue</span></span>
<span data-ttu-id="862c2-156">Specifica la parte non credenziale della stringa di connessione ODBC (Open Database Connectivity).</span><span class="sxs-lookup"><span data-stu-id="862c2-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="862c2-157">Questo parametro è applicabile solo per il servizio collegato ODBC.</span><span class="sxs-lookup"><span data-stu-id="862c2-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="862c2-158">-ResourceGroupName</span></span>
<span data-ttu-id="862c2-159">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="862c2-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="862c2-160">Questo cmdlet crittografa i dati per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="862c2-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-161">-Server</span><span class="sxs-lookup"><span data-stu-id="862c2-161">-Server</span></span>
<span data-ttu-id="862c2-162">Specifica il nome del server del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="862c2-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-163">-Digitare</span><span class="sxs-lookup"><span data-stu-id="862c2-163">-Type</span></span>
<span data-ttu-id="862c2-164">Specifica il tipo di servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="862c2-164">Specifies the linked service type.</span></span>
<span data-ttu-id="862c2-165">Questo cmdlet crittografa i dati per il tipo di servizio collegato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="862c2-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="862c2-166">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="862c2-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="862c2-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="862c2-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="862c2-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="862c2-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="862c2-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="862c2-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="862c2-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="862c2-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="862c2-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="862c2-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-176">-Valore</span><span class="sxs-lookup"><span data-stu-id="862c2-176">-Value</span></span>
<span data-ttu-id="862c2-177">Specifica il valore da crittografare.</span><span class="sxs-lookup"><span data-stu-id="862c2-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="862c2-178">Per un servizio collegato a SQL Server locale e un servizio collegato Oracle locale, usare una stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="862c2-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="862c2-179">Per un servizio collegato ODBC locale, usare la parte relativa alle credenziali della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="862c2-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="862c2-180">Per il servizio collegato al file System in locale, se il file System è locale per il computer gateway, USA local o localhost e se il file System si trova in un server diverso dal computer gateway, USA \\ \\ nomeserver.</span><span class="sxs-lookup"><span data-stu-id="862c2-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862c2-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862c2-181">CommonParameters</span></span>
<span data-ttu-id="862c2-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="862c2-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862c2-183">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862c2-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862c2-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="862c2-184">INPUTS</span></span>

### <span data-ttu-id="862c2-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="862c2-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="862c2-186">System. String</span><span class="sxs-lookup"><span data-stu-id="862c2-186">System.String</span></span>

## <span data-ttu-id="862c2-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="862c2-187">OUTPUTS</span></span>

### <span data-ttu-id="862c2-188">System. String</span><span class="sxs-lookup"><span data-stu-id="862c2-188">System.String</span></span>

## <span data-ttu-id="862c2-189">Note</span><span class="sxs-lookup"><span data-stu-id="862c2-189">NOTES</span></span>
* <span data-ttu-id="862c2-190">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="862c2-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="862c2-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="862c2-191">RELATED LINKS</span></span>

[<span data-ttu-id="862c2-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="862c2-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


