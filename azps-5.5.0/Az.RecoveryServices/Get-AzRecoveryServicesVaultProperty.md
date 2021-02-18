---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192926"
---
# <span data-ttu-id="e194b-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="e194b-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="e194b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e194b-102">SYNOPSIS</span></span>
<span data-ttu-id="e194b-103">Restituisce le proprietà di un Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e194b-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="e194b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e194b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e194b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e194b-105">DESCRIPTION</span></span>
<span data-ttu-id="e194b-106">Il **cmdlet Get-AzRecoveryServicesVaultProperty** restituisce le proprietà di un vault dei servizi di recupero.</span><span class="sxs-lookup"><span data-stu-id="e194b-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="e194b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e194b-107">EXAMPLES</span></span>

### <span data-ttu-id="e194b-108">Esempio 1: Ottenere le proprietà di un vault</span><span class="sxs-lookup"><span data-stu-id="e194b-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="e194b-109">Il primo comando ottiene un oggetto Vault e quindi lo archivia nella $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="e194b-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="e194b-110">Il secondo comando recupera le proprietà del Vault.</span><span class="sxs-lookup"><span data-stu-id="e194b-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="e194b-111">A questo punto si accede alle proprietà di crittografia del vault.</span><span class="sxs-lookup"><span data-stu-id="e194b-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="e194b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e194b-112">PARAMETERS</span></span>

### <span data-ttu-id="e194b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e194b-113">-DefaultProfile</span></span>
<span data-ttu-id="e194b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e194b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e194b-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e194b-115">-VaultId</span></span>
<span data-ttu-id="e194b-116">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e194b-116">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e194b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e194b-117">CommonParameters</span></span>
<span data-ttu-id="e194b-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e194b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e194b-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e194b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e194b-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="e194b-120">INPUTS</span></span>

### <span data-ttu-id="e194b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e194b-121">System.String</span></span>

## <span data-ttu-id="e194b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e194b-122">OUTPUTS</span></span>

### <span data-ttu-id="e194b-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="e194b-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="e194b-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="e194b-124">NOTES</span></span>

## <span data-ttu-id="e194b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e194b-125">RELATED LINKS</span></span>

[<span data-ttu-id="e194b-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e194b-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="e194b-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="e194b-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
