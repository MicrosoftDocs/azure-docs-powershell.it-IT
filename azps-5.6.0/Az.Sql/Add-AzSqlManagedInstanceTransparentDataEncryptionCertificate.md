---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 3a44d520e68fc1c2eec6593af728300a469760a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961501"
---
# <span data-ttu-id="75d6f-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="75d6f-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="75d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="75d6f-103">Aggiunge un certificato di crittografia dei dati trasparente per l'istanza gestita specificata</span><span class="sxs-lookup"><span data-stu-id="75d6f-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="75d6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75d6f-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75d6f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="75d6f-106">LAdd-AzSqlManagedInstanceTransparentDataEncryptionCertificate aggiunge un certificato di crittografia dei dati trasparente per l'istanza gestita specificata</span><span class="sxs-lookup"><span data-stu-id="75d6f-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="75d6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="75d6f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75d6f-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="75d6f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75d6f-109">PARAMETERS</span></span>

### <span data-ttu-id="75d6f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d6f-110">-DefaultProfile</span></span>
<span data-ttu-id="75d6f-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75d6f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d6f-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="75d6f-112">-ManagedInstanceName</span></span>
<span data-ttu-id="75d6f-113">Nome dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="75d6f-113">The managed instance name</span></span>

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

### <span data-ttu-id="75d6f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75d6f-114">-PassThru</span></span>
<span data-ttu-id="75d6f-115">In caso di esecuzione corretta, restituisce l'oggetto certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="75d6f-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="75d6f-116">-Password</span><span class="sxs-lookup"><span data-stu-id="75d6f-116">-Password</span></span>
<span data-ttu-id="75d6f-117">Password per il certificato di crittografia dati trasparente</span><span class="sxs-lookup"><span data-stu-id="75d6f-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="75d6f-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="75d6f-118">-PrivateBlob</span></span>
<span data-ttu-id="75d6f-119">BLOB privato per il certificato di crittografia dei dati trasparente</span><span class="sxs-lookup"><span data-stu-id="75d6f-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="75d6f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d6f-120">-ResourceGroupName</span></span>
<span data-ttu-id="75d6f-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="75d6f-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="75d6f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75d6f-122">-Confirm</span></span>
<span data-ttu-id="75d6f-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75d6f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d6f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d6f-124">-WhatIf</span></span>
<span data-ttu-id="75d6f-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75d6f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d6f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75d6f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d6f-127">CommonParameters</span></span>
<span data-ttu-id="75d6f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d6f-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75d6f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d6f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="75d6f-130">INPUTS</span></span>

### <span data-ttu-id="75d6f-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="75d6f-131">None</span></span>

## <span data-ttu-id="75d6f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75d6f-132">OUTPUTS</span></span>

### <span data-ttu-id="75d6f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75d6f-133">System.Boolean</span></span>

## <span data-ttu-id="75d6f-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="75d6f-134">NOTES</span></span>

## <span data-ttu-id="75d6f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75d6f-135">RELATED LINKS</span></span>
