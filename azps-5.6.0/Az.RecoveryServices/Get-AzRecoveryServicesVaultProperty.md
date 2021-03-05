---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4e0b74ead08a3b944e66b46a6fee0fb71976b223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973645"
---
# <span data-ttu-id="41737-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="41737-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="41737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41737-102">SYNOPSIS</span></span>
<span data-ttu-id="41737-103">Restituisce le proprietà di un Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="41737-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="41737-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41737-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41737-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41737-105">DESCRIPTION</span></span>
<span data-ttu-id="41737-106">Il **cmdlet Get-AzRecoveryServicesVaultProperty** restituisce le proprietà di un vault dei servizi di recupero.</span><span class="sxs-lookup"><span data-stu-id="41737-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="41737-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41737-107">EXAMPLES</span></span>

### <span data-ttu-id="41737-108">Esempio 1: Ottenere le proprietà di un vault</span><span class="sxs-lookup"><span data-stu-id="41737-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="41737-109">Il primo comando ottiene un oggetto Vault e quindi lo archivia nella $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="41737-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="41737-110">Il secondo comando recupera le proprietà del Vault.</span><span class="sxs-lookup"><span data-stu-id="41737-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="41737-111">A questo punto si accede alle proprietà di crittografia del vault.</span><span class="sxs-lookup"><span data-stu-id="41737-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="41737-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41737-112">PARAMETERS</span></span>

### <span data-ttu-id="41737-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41737-113">-DefaultProfile</span></span>
<span data-ttu-id="41737-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41737-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41737-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="41737-115">-VaultId</span></span>
<span data-ttu-id="41737-116">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="41737-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="41737-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41737-117">CommonParameters</span></span>
<span data-ttu-id="41737-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41737-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41737-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41737-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41737-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="41737-120">INPUTS</span></span>

### <span data-ttu-id="41737-121">System.String</span><span class="sxs-lookup"><span data-stu-id="41737-121">System.String</span></span>

## <span data-ttu-id="41737-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41737-122">OUTPUTS</span></span>

### <span data-ttu-id="41737-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="41737-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="41737-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="41737-124">NOTES</span></span>

## <span data-ttu-id="41737-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41737-125">RELATED LINKS</span></span>

[<span data-ttu-id="41737-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="41737-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="41737-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="41737-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
