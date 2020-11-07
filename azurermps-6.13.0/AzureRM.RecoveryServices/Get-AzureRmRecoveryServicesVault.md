---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 0812fc8aa5673f6475fb822137cffff025003d32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688378"
---
# <span data-ttu-id="4f4eb-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4f4eb-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="4f4eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4eb-103">Ottiene un elenco dei Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f4eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f4eb-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f4eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4f4eb-106">Il cmdlet **Get-AzureRmRecoveryServicesVault** ottiene un elenco dei Vault di servizi di recupero nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="4f4eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f4eb-107">EXAMPLES</span></span>

### <span data-ttu-id="4f4eb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f4eb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="4f4eb-109">Ottenere l'elenco di Vault nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="4f4eb-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4f4eb-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="4f4eb-111">Ottenere l'elenco di Vault nel gruppo di risorse nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="4f4eb-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4f4eb-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="4f4eb-113">Ottenere il Vault nel gruppo di risorse con il nome assegnato.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="4f4eb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f4eb-114">PARAMETERS</span></span>

### <span data-ttu-id="4f4eb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f4eb-115">-Name</span></span>
<span data-ttu-id="4f4eb-116">Specifica il nome del Vault a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f4eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f4eb-118">Specifica il nome del gruppo di risorse Azure in cui creare o da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4eb-119">-DefaultProfile</span></span>
<span data-ttu-id="4f4eb-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4eb-121">CommonParameters</span></span>
<span data-ttu-id="4f4eb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f4eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4eb-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4eb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4eb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f4eb-124">INPUTS</span></span>

### <span data-ttu-id="4f4eb-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4f4eb-125">None</span></span>

## <span data-ttu-id="4f4eb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f4eb-126">OUTPUTS</span></span>

### <span data-ttu-id="4f4eb-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="4f4eb-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4f4eb-128">Note</span><span class="sxs-lookup"><span data-stu-id="4f4eb-128">NOTES</span></span>

## <span data-ttu-id="4f4eb-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f4eb-129">RELATED LINKS</span></span>

[<span data-ttu-id="4f4eb-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4f4eb-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4f4eb-131">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4f4eb-131">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="4f4eb-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4f4eb-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


