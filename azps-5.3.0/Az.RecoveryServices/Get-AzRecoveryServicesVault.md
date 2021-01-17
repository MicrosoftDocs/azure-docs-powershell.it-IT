---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475002"
---
# <span data-ttu-id="565fa-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="565fa-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="565fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="565fa-102">SYNOPSIS</span></span>

<span data-ttu-id="565fa-103">Ottiene un elenco dei Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="565fa-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="565fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="565fa-104">SYNTAX</span></span>

### <span data-ttu-id="565fa-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="565fa-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="565fa-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="565fa-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="565fa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="565fa-107">DESCRIPTION</span></span>

<span data-ttu-id="565fa-108">Il cmdlet **Get-AzRecoveryServicesVault** ottiene un elenco dei Vault di servizi di recupero nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="565fa-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="565fa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="565fa-109">EXAMPLES</span></span>

### <span data-ttu-id="565fa-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="565fa-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="565fa-111">Ottenere l'elenco di Vault nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="565fa-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="565fa-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="565fa-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="565fa-113">Ottenere l'elenco di Vault nel gruppo di risorse nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="565fa-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="565fa-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="565fa-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="565fa-115">Il primo cmdlet ottiene il Vault nel gruppo di risorse con il nome assegnato.</span><span class="sxs-lookup"><span data-stu-id="565fa-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="565fa-116">Accediamo quindi alle informazioni MSI dal Vault.</span><span class="sxs-lookup"><span data-stu-id="565fa-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="565fa-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="565fa-117">PARAMETERS</span></span>

### <span data-ttu-id="565fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565fa-118">-DefaultProfile</span></span>

<span data-ttu-id="565fa-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="565fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="565fa-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="565fa-120">-Name</span></span>

<span data-ttu-id="565fa-121">Specifica il nome del Vault a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="565fa-121">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="565fa-122">-ResourceGroupName</span></span>

<span data-ttu-id="565fa-123">Specifica il nome del gruppo di risorse Azure da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="565fa-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565fa-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="565fa-124">-Tag</span></span>

<span data-ttu-id="565fa-125">Specifica i tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="565fa-125">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565fa-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="565fa-126">-TagName</span></span>

<span data-ttu-id="565fa-127">Specifica la chiave del tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="565fa-127">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565fa-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="565fa-128">-TagValue</span></span>

<span data-ttu-id="565fa-129">Specifica il valore del tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="565fa-129">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="565fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565fa-130">CommonParameters</span></span>
<span data-ttu-id="565fa-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565fa-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="565fa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565fa-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="565fa-133">INPUTS</span></span>

### <span data-ttu-id="565fa-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="565fa-134">None</span></span>

## <span data-ttu-id="565fa-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="565fa-135">OUTPUTS</span></span>

### <span data-ttu-id="565fa-136">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="565fa-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="565fa-137">Note</span><span class="sxs-lookup"><span data-stu-id="565fa-137">NOTES</span></span>
<span data-ttu-id="565fa-138">Get-AzRecoveryServicesVault nella versione precedente di AZ. RecoveryServices (<= 2.10.0) non può funzionare con AZ. Accounts (>= 1.8.1) a causa di riferimenti di assembly non corretti.</span><span class="sxs-lookup"><span data-stu-id="565fa-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="565fa-139">Il modulo AZ. RecoveryServices deve essere aggiornato a 2.11.0 o più recente se si usano gli account AZ o AZ più recenti.</span><span class="sxs-lookup"><span data-stu-id="565fa-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="565fa-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="565fa-140">RELATED LINKS</span></span>

[<span data-ttu-id="565fa-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="565fa-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="565fa-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="565fa-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="565fa-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="565fa-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
