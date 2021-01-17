---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: 6e4f58c355296a281a9ecbef21d7eca754bf41c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476192"
---
# <span data-ttu-id="2cc48-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cc48-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="2cc48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cc48-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc48-103">Definizioni dei ruoli di elenco di un HSM gestito specifico in un ambito specifico.</span><span class="sxs-lookup"><span data-stu-id="2cc48-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="2cc48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cc48-104">SYNTAX</span></span>

### <span data-ttu-id="2cc48-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cc48-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cc48-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2cc48-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc48-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cc48-107">DESCRIPTION</span></span>
<span data-ttu-id="2cc48-108">Definizioni dei ruoli di elenco di un HSM gestito specifico in un ambito specifico.</span><span class="sxs-lookup"><span data-stu-id="2cc48-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="2cc48-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cc48-109">EXAMPLES</span></span>

### <span data-ttu-id="2cc48-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cc48-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="2cc48-111">Nell'esempio vengono elencati tutti i ruoli in ambito "/Keys".</span><span class="sxs-lookup"><span data-stu-id="2cc48-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="2cc48-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2cc48-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="2cc48-113">L'esempio ottiene il ruolo "Managed HSM backup" e controlla le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="2cc48-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="2cc48-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cc48-114">PARAMETERS</span></span>

### <span data-ttu-id="2cc48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc48-115">-DefaultProfile</span></span>
<span data-ttu-id="2cc48-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cc48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cc48-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="2cc48-117">-HsmName</span></span>
<span data-ttu-id="2cc48-118">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="2cc48-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="2cc48-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2cc48-119">-RoleDefinitionName</span></span>
<span data-ttu-id="2cc48-120">Nome della definizione del ruolo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2cc48-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc48-121">-Ambito</span><span class="sxs-lookup"><span data-stu-id="2cc48-121">-Scope</span></span>
<span data-ttu-id="2cc48-122">Ambito a cui si applica l'assegnazione di ruolo o la definizione, ad esempio "/" o "/Keys" o "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="2cc48-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="2cc48-123">Quando viene omesso, viene usato "/".</span><span class="sxs-lookup"><span data-stu-id="2cc48-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc48-124">CommonParameters</span></span>
<span data-ttu-id="2cc48-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc48-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cc48-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc48-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cc48-127">INPUTS</span></span>

### <span data-ttu-id="2cc48-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2cc48-128">None</span></span>

## <span data-ttu-id="2cc48-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cc48-129">OUTPUTS</span></span>

### <span data-ttu-id="2cc48-130">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cc48-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="2cc48-131">Note</span><span class="sxs-lookup"><span data-stu-id="2cc48-131">NOTES</span></span>

## <span data-ttu-id="2cc48-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cc48-132">RELATED LINKS</span></span>
