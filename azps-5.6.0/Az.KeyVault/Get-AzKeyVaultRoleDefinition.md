---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: b5d5da8c02081437f064fc1d2a6a29a5b772e8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001437"
---
# <span data-ttu-id="d1ec4-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d1ec4-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="d1ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ec4-103">Elencare le definizioni di un determinato HSM gestito in un ambito specifico.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="d1ec4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1ec4-104">SYNTAX</span></span>

### <span data-ttu-id="d1ec4-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1ec4-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ec4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d1ec4-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1ec4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1ec4-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ec4-108">Elencare le definizioni di un determinato HSM gestito in un ambito specifico.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="d1ec4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1ec4-109">EXAMPLES</span></span>

### <span data-ttu-id="d1ec4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1ec4-110">Example 1</span></span>
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

<span data-ttu-id="d1ec4-111">L'esempio elenca tutti i ruoli nell'ambito "/keys".</span><span class="sxs-lookup"><span data-stu-id="d1ec4-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="d1ec4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d1ec4-112">Example 2</span></span>
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

<span data-ttu-id="d1ec4-113">L'esempio ottiene il ruolo "Managed HSM Backup" e ne esamina le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="d1ec4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1ec4-114">PARAMETERS</span></span>

### <span data-ttu-id="d1ec4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ec4-115">-DefaultProfile</span></span>
<span data-ttu-id="d1ec4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1ec4-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d1ec4-117">-HsmName</span></span>
<span data-ttu-id="d1ec4-118">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="d1ec4-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d1ec4-119">-RoleDefinitionName</span></span>
<span data-ttu-id="d1ec4-120">Nome della definizione di ruolo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="d1ec4-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="d1ec4-121">-Scope</span></span>
<span data-ttu-id="d1ec4-122">Ambito in cui si applica l'assegnazione o la definizione di ruolo, ad esempio '/' o '/keys' o '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="d1ec4-123">'/' viene usato quando viene omesso.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="d1ec4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ec4-124">CommonParameters</span></span>
<span data-ttu-id="d1ec4-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ec4-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ec4-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1ec4-127">INPUTS</span></span>

### <span data-ttu-id="d1ec4-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1ec4-128">None</span></span>

## <span data-ttu-id="d1ec4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1ec4-129">OUTPUTS</span></span>

### <span data-ttu-id="d1ec4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d1ec4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="d1ec4-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1ec4-131">NOTES</span></span>

## <span data-ttu-id="d1ec4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1ec4-132">RELATED LINKS</span></span>
