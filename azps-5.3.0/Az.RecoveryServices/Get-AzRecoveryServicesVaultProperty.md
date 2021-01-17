---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475003"
---
# <span data-ttu-id="09406-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="09406-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="09406-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09406-102">SYNOPSIS</span></span>
<span data-ttu-id="09406-103">Restituisce le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="09406-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="09406-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09406-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09406-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09406-105">DESCRIPTION</span></span>
<span data-ttu-id="09406-106">Il cmdlet **Get-AzRecoveryServicesVaultProperty** restituisce le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="09406-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="09406-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09406-107">EXAMPLES</span></span>

### <span data-ttu-id="09406-108">Esempio 1: ottenere le proprietà di un Vault</span><span class="sxs-lookup"><span data-stu-id="09406-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="09406-109">Il primo comando ottiene un oggetto Vault e lo archivia nella variabile $vault.</span><span class="sxs-lookup"><span data-stu-id="09406-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="09406-110">Il secondo comando recupera le proprietà del Vault.</span><span class="sxs-lookup"><span data-stu-id="09406-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="09406-111">Si accede quindi alla encryptionProperties del Vault.</span><span class="sxs-lookup"><span data-stu-id="09406-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="09406-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09406-112">PARAMETERS</span></span>

### <span data-ttu-id="09406-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09406-113">-DefaultProfile</span></span>
<span data-ttu-id="09406-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09406-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09406-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="09406-115">-VaultId</span></span>
<span data-ttu-id="09406-116">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="09406-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="09406-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09406-117">CommonParameters</span></span>
<span data-ttu-id="09406-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09406-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09406-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09406-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09406-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09406-120">INPUTS</span></span>

### <span data-ttu-id="09406-121">System. String</span><span class="sxs-lookup"><span data-stu-id="09406-121">System.String</span></span>

## <span data-ttu-id="09406-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09406-122">OUTPUTS</span></span>

### <span data-ttu-id="09406-123">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="09406-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="09406-124">Note</span><span class="sxs-lookup"><span data-stu-id="09406-124">NOTES</span></span>

## <span data-ttu-id="09406-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09406-125">RELATED LINKS</span></span>

[<span data-ttu-id="09406-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="09406-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="09406-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="09406-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
