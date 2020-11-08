---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022673"
---
# <span data-ttu-id="d9bcd-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="d9bcd-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="d9bcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bcd-103">Restituisce le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d9bcd-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="d9bcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9bcd-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9bcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bcd-106">Il cmdlet **Get-AzRecoveryServicesVaultProperty** restituisce le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d9bcd-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="d9bcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9bcd-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bcd-108">Esempio 1: ottenere le proprietà di un Vault</span><span class="sxs-lookup"><span data-stu-id="d9bcd-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="d9bcd-109">Il primo comando ottiene un oggetto Vault e lo archivia nella variabile $vault.</span><span class="sxs-lookup"><span data-stu-id="d9bcd-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="d9bcd-110">Il secondo comando recupera le proprietà del Vault.</span><span class="sxs-lookup"><span data-stu-id="d9bcd-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="d9bcd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9bcd-111">PARAMETERS</span></span>

### <span data-ttu-id="d9bcd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bcd-112">-DefaultProfile</span></span>
<span data-ttu-id="d9bcd-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9bcd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bcd-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d9bcd-114">-VaultId</span></span>
<span data-ttu-id="d9bcd-115">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d9bcd-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d9bcd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bcd-116">CommonParameters</span></span>
<span data-ttu-id="d9bcd-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bcd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bcd-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9bcd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bcd-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9bcd-119">INPUTS</span></span>

### <span data-ttu-id="d9bcd-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d9bcd-120">System.String</span></span>

## <span data-ttu-id="d9bcd-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9bcd-121">OUTPUTS</span></span>

### <span data-ttu-id="d9bcd-122">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="d9bcd-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="d9bcd-123">Note</span><span class="sxs-lookup"><span data-stu-id="d9bcd-123">NOTES</span></span>

## <span data-ttu-id="d9bcd-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9bcd-124">RELATED LINKS</span></span>

[<span data-ttu-id="d9bcd-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d9bcd-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="d9bcd-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="d9bcd-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
