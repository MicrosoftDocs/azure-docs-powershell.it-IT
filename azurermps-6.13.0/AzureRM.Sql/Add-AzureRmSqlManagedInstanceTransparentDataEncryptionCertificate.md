---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 9fe8e36a752b4643ba44a59e8c44954bf25284c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686040"
---
# <span data-ttu-id="8f696-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8f696-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="8f696-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f696-102">SYNOPSIS</span></span>
<span data-ttu-id="8f696-103">Aggiunge un certificato di crittografia dati trasparente per l'istanza gestita specificata</span><span class="sxs-lookup"><span data-stu-id="8f696-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f696-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f696-104">SYNTAX</span></span>

```
Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f696-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f696-105">DESCRIPTION</span></span>
<span data-ttu-id="8f696-106">Il Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate aggiunge un certificato di crittografia dati trasparente per l'istanza gestita specificata</span><span class="sxs-lookup"><span data-stu-id="8f696-106">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="8f696-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f696-107">EXAMPLES</span></span>

### <span data-ttu-id="8f696-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f696-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="8f696-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f696-109">PARAMETERS</span></span>

### <span data-ttu-id="8f696-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f696-110">-DefaultProfile</span></span>
<span data-ttu-id="8f696-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f696-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f696-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="8f696-112">-ManagedInstanceName</span></span>
<span data-ttu-id="8f696-113">Nome dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="8f696-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f696-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f696-114">-PassThru</span></span>
<span data-ttu-id="8f696-115">Per l'esecuzione corretta, restituisce l'oggetto certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="8f696-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="8f696-116">-Password</span><span class="sxs-lookup"><span data-stu-id="8f696-116">-Password</span></span>
<span data-ttu-id="8f696-117">Password per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="8f696-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f696-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="8f696-118">-PrivateBlob</span></span>
<span data-ttu-id="8f696-119">Il BLOB privato per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="8f696-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="8f696-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f696-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f696-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8f696-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f696-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f696-122">-Confirm</span></span>
<span data-ttu-id="8f696-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f696-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f696-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f696-124">-WhatIf</span></span>
<span data-ttu-id="8f696-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f696-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f696-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f696-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f696-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f696-127">CommonParameters</span></span>
<span data-ttu-id="8f696-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f696-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f696-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f696-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f696-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f696-130">INPUTS</span></span>

### <span data-ttu-id="8f696-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8f696-131">None</span></span>

## <span data-ttu-id="8f696-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f696-132">OUTPUTS</span></span>

### <span data-ttu-id="8f696-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f696-133">System.Boolean</span></span>

## <span data-ttu-id="8f696-134">Note</span><span class="sxs-lookup"><span data-stu-id="8f696-134">NOTES</span></span>

## <span data-ttu-id="8f696-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f696-135">RELATED LINKS</span></span>
