---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363943"
---
# <span data-ttu-id="e0d28-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e0d28-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="e0d28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0d28-102">SYNOPSIS</span></span>

<span data-ttu-id="e0d28-103">Ottiene un elenco dei Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e0d28-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="e0d28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0d28-104">SYNTAX</span></span>

### <span data-ttu-id="e0d28-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0d28-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0d28-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0d28-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0d28-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0d28-107">DESCRIPTION</span></span>

<span data-ttu-id="e0d28-108">Il cmdlet **Get-AzRecoveryServicesVault** ottiene un elenco dei Vault di servizi di recupero nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e0d28-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="e0d28-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0d28-109">EXAMPLES</span></span>

### <span data-ttu-id="e0d28-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0d28-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="e0d28-111">Ottenere l'elenco di Vault nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="e0d28-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="e0d28-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e0d28-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="e0d28-113">Ottenere l'elenco di Vault nel gruppo di risorse nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="e0d28-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="e0d28-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e0d28-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="e0d28-115">Ottenere il Vault nel gruppo di risorse con il nome assegnato.</span><span class="sxs-lookup"><span data-stu-id="e0d28-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="e0d28-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0d28-116">PARAMETERS</span></span>

### <span data-ttu-id="e0d28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d28-117">-DefaultProfile</span></span>

<span data-ttu-id="e0d28-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d28-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0d28-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0d28-119">-Name</span></span>

<span data-ttu-id="e0d28-120">Specifica il nome del Vault a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="e0d28-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="e0d28-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d28-121">-ResourceGroupName</span></span>

<span data-ttu-id="e0d28-122">Specifica il nome del gruppo di risorse Azure da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="e0d28-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="e0d28-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0d28-123">-Tag</span></span>

<span data-ttu-id="e0d28-124">Specifica i tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="e0d28-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="e0d28-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="e0d28-125">-TagName</span></span>

<span data-ttu-id="e0d28-126">Specifica la chiave del tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="e0d28-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="e0d28-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="e0d28-127">-TagValue</span></span>

<span data-ttu-id="e0d28-128">Specifica il valore del tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="e0d28-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="e0d28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d28-129">CommonParameters</span></span>
<span data-ttu-id="e0d28-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d28-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0d28-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d28-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0d28-132">INPUTS</span></span>

### <span data-ttu-id="e0d28-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e0d28-133">None</span></span>

## <span data-ttu-id="e0d28-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0d28-134">OUTPUTS</span></span>

### <span data-ttu-id="e0d28-135">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e0d28-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e0d28-136">Note</span><span class="sxs-lookup"><span data-stu-id="e0d28-136">NOTES</span></span>
<span data-ttu-id="e0d28-137">Get-AzRecoveryServicesVault nella versione precedente di AZ. RecoveryServices (<= 2.10.0) non può funzionare con AZ. Accounts (>= 1.8.1) a causa di riferimenti di assembly non corretti.</span><span class="sxs-lookup"><span data-stu-id="e0d28-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="e0d28-138">Il modulo AZ. RecoveryServices deve essere aggiornato a 2.11.0 o più recente se si usano gli account AZ o AZ più recenti.</span><span class="sxs-lookup"><span data-stu-id="e0d28-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="e0d28-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0d28-139">RELATED LINKS</span></span>

[<span data-ttu-id="e0d28-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e0d28-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e0d28-141">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e0d28-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="e0d28-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e0d28-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
