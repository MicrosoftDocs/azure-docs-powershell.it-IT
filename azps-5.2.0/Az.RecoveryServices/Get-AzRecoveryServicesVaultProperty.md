---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337759"
---
# <span data-ttu-id="4eae4-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="4eae4-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="4eae4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4eae4-102">SYNOPSIS</span></span>
<span data-ttu-id="4eae4-103">Restituisce le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4eae4-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="4eae4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4eae4-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4eae4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4eae4-105">DESCRIPTION</span></span>
<span data-ttu-id="4eae4-106">Il cmdlet **Get-AzRecoveryServicesVaultProperty** restituisce le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4eae4-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="4eae4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4eae4-107">EXAMPLES</span></span>

### <span data-ttu-id="4eae4-108">Esempio 1: ottenere le proprietà di un Vault</span><span class="sxs-lookup"><span data-stu-id="4eae4-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="4eae4-109">Il primo comando ottiene un oggetto Vault e lo archivia nella variabile $vault.</span><span class="sxs-lookup"><span data-stu-id="4eae4-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="4eae4-110">Il secondo comando recupera le proprietà del Vault.</span><span class="sxs-lookup"><span data-stu-id="4eae4-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="4eae4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4eae4-111">PARAMETERS</span></span>

### <span data-ttu-id="4eae4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eae4-112">-DefaultProfile</span></span>
<span data-ttu-id="4eae4-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4eae4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eae4-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4eae4-114">-VaultId</span></span>
<span data-ttu-id="4eae4-115">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4eae4-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4eae4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eae4-116">CommonParameters</span></span>
<span data-ttu-id="4eae4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eae4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eae4-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eae4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eae4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4eae4-119">INPUTS</span></span>

### <span data-ttu-id="4eae4-120">System. String</span><span class="sxs-lookup"><span data-stu-id="4eae4-120">System.String</span></span>

## <span data-ttu-id="4eae4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4eae4-121">OUTPUTS</span></span>

### <span data-ttu-id="4eae4-122">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="4eae4-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="4eae4-123">Note</span><span class="sxs-lookup"><span data-stu-id="4eae4-123">NOTES</span></span>

## <span data-ttu-id="4eae4-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4eae4-124">RELATED LINKS</span></span>

[<span data-ttu-id="4eae4-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4eae4-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="4eae4-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="4eae4-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
