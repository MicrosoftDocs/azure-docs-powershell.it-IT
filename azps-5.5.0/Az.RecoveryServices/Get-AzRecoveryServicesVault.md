---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192935"
---
# <span data-ttu-id="472f7-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="472f7-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="472f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="472f7-102">SYNOPSIS</span></span>

<span data-ttu-id="472f7-103">Ottiene un elenco di vault di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="472f7-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="472f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="472f7-104">SYNTAX</span></span>

### <span data-ttu-id="472f7-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="472f7-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="472f7-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="472f7-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="472f7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="472f7-107">DESCRIPTION</span></span>

<span data-ttu-id="472f7-108">Il cmdlet **Get-AzRecoveryServicesVault** ottiene un elenco di vault dei servizi di ripristino nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="472f7-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="472f7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="472f7-109">EXAMPLES</span></span>

### <span data-ttu-id="472f7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="472f7-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="472f7-111">Ottenere l'elenco del vault nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="472f7-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="472f7-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="472f7-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="472f7-113">Ottenere l'elenco del vault nel gruppo di risorse nella sottoscrizione selezionata.</span><span class="sxs-lookup"><span data-stu-id="472f7-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="472f7-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="472f7-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="472f7-115">Il primo cmdlet ottiene il vault nel gruppo di risorse con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="472f7-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="472f7-116">A questo punto si accede alle informazioni MSI dal Vault.</span><span class="sxs-lookup"><span data-stu-id="472f7-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="472f7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="472f7-117">PARAMETERS</span></span>

### <span data-ttu-id="472f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472f7-118">-DefaultProfile</span></span>

<span data-ttu-id="472f7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="472f7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="472f7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="472f7-120">-Name</span></span>

<span data-ttu-id="472f7-121">Specifica il nome del vault per cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="472f7-121">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="472f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="472f7-122">-ResourceGroupName</span></span>

<span data-ttu-id="472f7-123">Specifica il nome del gruppo di risorse azure da cui recuperare l'oggetto dei servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="472f7-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="472f7-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="472f7-124">-Tag</span></span>

<span data-ttu-id="472f7-125">Specifica i tag per cui eseguire la query</span><span class="sxs-lookup"><span data-stu-id="472f7-125">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="472f7-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="472f7-126">-TagName</span></span>

<span data-ttu-id="472f7-127">Specifica la chiave del tag per cui eseguire la query</span><span class="sxs-lookup"><span data-stu-id="472f7-127">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="472f7-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="472f7-128">-TagValue</span></span>

<span data-ttu-id="472f7-129">Specifica il valore del tag per cui eseguire la query</span><span class="sxs-lookup"><span data-stu-id="472f7-129">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="472f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472f7-130">CommonParameters</span></span>
<span data-ttu-id="472f7-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="472f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472f7-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="472f7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472f7-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="472f7-133">INPUTS</span></span>

### <span data-ttu-id="472f7-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="472f7-134">None</span></span>

## <span data-ttu-id="472f7-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="472f7-135">OUTPUTS</span></span>

### <span data-ttu-id="472f7-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="472f7-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="472f7-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="472f7-137">NOTES</span></span>
<span data-ttu-id="472f7-138">Get-AzRecoveryServicesVault nella versione precedente di Az.RecoveryServices(<=2.10.0) non può funzionare con Az.Accounts(>=1.8.1) a causa di un riferimento all'assembly errato.</span><span class="sxs-lookup"><span data-stu-id="472f7-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="472f7-139">Il modulo Az.RecoveryServices deve essere aggiornato alla versione 2.11.0 o versione più recente se si usa la versione più recente di Az o Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="472f7-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="472f7-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="472f7-140">RELATED LINKS</span></span>

[<span data-ttu-id="472f7-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="472f7-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="472f7-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="472f7-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="472f7-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="472f7-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
