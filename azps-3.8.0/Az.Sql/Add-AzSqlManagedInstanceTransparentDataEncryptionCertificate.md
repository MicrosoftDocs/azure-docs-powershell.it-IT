---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019227"
---
# <span data-ttu-id="09637-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="09637-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="09637-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09637-102">SYNOPSIS</span></span>
<span data-ttu-id="09637-103">Aggiunge un certificato di crittografia dati trasparente per l'istanza gestita specificata</span><span class="sxs-lookup"><span data-stu-id="09637-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="09637-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09637-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09637-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09637-105">DESCRIPTION</span></span>
<span data-ttu-id="09637-106">Il Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate aggiunge un certificato di crittografia dati trasparente per l'istanza gestita specificata</span><span class="sxs-lookup"><span data-stu-id="09637-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="09637-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09637-107">EXAMPLES</span></span>

### <span data-ttu-id="09637-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09637-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="09637-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09637-109">PARAMETERS</span></span>

### <span data-ttu-id="09637-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09637-110">-DefaultProfile</span></span>
<span data-ttu-id="09637-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09637-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09637-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="09637-112">-ManagedInstanceName</span></span>
<span data-ttu-id="09637-113">Nome dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="09637-113">The managed instance name</span></span>

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

### <span data-ttu-id="09637-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09637-114">-PassThru</span></span>
<span data-ttu-id="09637-115">Per l'esecuzione corretta, restituisce l'oggetto certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="09637-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="09637-116">-Password</span><span class="sxs-lookup"><span data-stu-id="09637-116">-Password</span></span>
<span data-ttu-id="09637-117">Password per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="09637-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="09637-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="09637-118">-PrivateBlob</span></span>
<span data-ttu-id="09637-119">Il BLOB privato per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="09637-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="09637-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09637-120">-ResourceGroupName</span></span>
<span data-ttu-id="09637-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="09637-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="09637-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09637-122">-Confirm</span></span>
<span data-ttu-id="09637-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09637-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09637-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09637-124">-WhatIf</span></span>
<span data-ttu-id="09637-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09637-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09637-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09637-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09637-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09637-127">CommonParameters</span></span>
<span data-ttu-id="09637-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09637-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09637-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09637-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09637-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09637-130">INPUTS</span></span>

### <span data-ttu-id="09637-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09637-131">None</span></span>

## <span data-ttu-id="09637-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09637-132">OUTPUTS</span></span>

### <span data-ttu-id="09637-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09637-133">System.Boolean</span></span>

## <span data-ttu-id="09637-134">Note</span><span class="sxs-lookup"><span data-stu-id="09637-134">NOTES</span></span>

## <span data-ttu-id="09637-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09637-135">RELATED LINKS</span></span>
