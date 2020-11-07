---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677639"
---
# <span data-ttu-id="7e081-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7e081-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="7e081-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e081-102">SYNOPSIS</span></span>
<span data-ttu-id="7e081-103">Ottiene un elenco dei Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7e081-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="7e081-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e081-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e081-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e081-105">DESCRIPTION</span></span>
<span data-ttu-id="7e081-106">Il cmdlet **Get-AzRecoveryServicesVault** ottiene un elenco dei Vault di servizi di recupero nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7e081-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="7e081-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e081-107">EXAMPLES</span></span>

### <span data-ttu-id="7e081-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e081-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="7e081-109">Ottenere l'elenco di Vault nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="7e081-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="7e081-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7e081-110">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="7e081-111">Ottenere l'elenco di Vault nel gruppo di risorse nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="7e081-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="7e081-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7e081-112">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="7e081-113">Ottenere il Vault nel gruppo di risorse con il nome assegnato.</span><span class="sxs-lookup"><span data-stu-id="7e081-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="7e081-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e081-114">PARAMETERS</span></span>

### <span data-ttu-id="7e081-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e081-115">-DefaultProfile</span></span>
<span data-ttu-id="7e081-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e081-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e081-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e081-117">-Name</span></span>
<span data-ttu-id="7e081-118">Specifica il nome del Vault a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="7e081-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="7e081-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e081-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e081-120">Specifica il nome del gruppo di risorse Azure in cui creare o da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="7e081-120">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="7e081-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e081-121">CommonParameters</span></span>
<span data-ttu-id="7e081-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e081-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e081-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e081-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e081-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e081-124">INPUTS</span></span>

### <span data-ttu-id="7e081-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7e081-125">None</span></span>

## <span data-ttu-id="7e081-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e081-126">OUTPUTS</span></span>

### <span data-ttu-id="7e081-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="7e081-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7e081-128">Note</span><span class="sxs-lookup"><span data-stu-id="7e081-128">NOTES</span></span>

## <span data-ttu-id="7e081-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e081-129">RELATED LINKS</span></span>

[<span data-ttu-id="7e081-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7e081-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7e081-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7e081-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="7e081-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7e081-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


