---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519990"
---
# <span data-ttu-id="b3fdc-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b3fdc-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="b3fdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fdc-103">Ottiene un elenco dei Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3fdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3fdc-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3fdc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="b3fdc-106">Il cmdlet **Get-AzureRmRecoveryServicesVault** ottiene un elenco dei Vault di servizi di recupero nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="b3fdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3fdc-107">EXAMPLES</span></span>

## <span data-ttu-id="b3fdc-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3fdc-108">PARAMETERS</span></span>

### <span data-ttu-id="b3fdc-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3fdc-109">-Name</span></span>
<span data-ttu-id="b3fdc-110">Specifica il nome del Vault a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-110">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="b3fdc-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3fdc-111">-ResourceGroupName</span></span>
<span data-ttu-id="b3fdc-112">Specifica il nome del gruppo di risorse Azure in cui creare o da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="b3fdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3fdc-113">-DefaultProfile</span></span>
<span data-ttu-id="b3fdc-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3fdc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fdc-115">CommonParameters</span></span>
<span data-ttu-id="b3fdc-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3fdc-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3fdc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fdc-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3fdc-118">INPUTS</span></span>

## <span data-ttu-id="b3fdc-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3fdc-119">OUTPUTS</span></span>

### <span data-ttu-id="b3fdc-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="b3fdc-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="b3fdc-121">Note</span><span class="sxs-lookup"><span data-stu-id="b3fdc-121">NOTES</span></span>

## <span data-ttu-id="b3fdc-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3fdc-122">RELATED LINKS</span></span>

[<span data-ttu-id="b3fdc-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b3fdc-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b3fdc-124">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b3fdc-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b3fdc-125">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b3fdc-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


