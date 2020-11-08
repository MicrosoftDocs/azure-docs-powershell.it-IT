---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: b7ee6a380bf7803913f3f302bee45bad62f106b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022674"
---
# <span data-ttu-id="288a9-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="288a9-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="288a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="288a9-102">SYNOPSIS</span></span>

<span data-ttu-id="288a9-103">Ottiene un elenco dei Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="288a9-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="288a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="288a9-104">SYNTAX</span></span>

### <span data-ttu-id="288a9-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="288a9-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="288a9-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="288a9-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="288a9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="288a9-107">DESCRIPTION</span></span>

<span data-ttu-id="288a9-108">Il cmdlet **Get-AzRecoveryServicesVault** ottiene un elenco dei Vault di servizi di recupero nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="288a9-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="288a9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="288a9-109">EXAMPLES</span></span>

### <span data-ttu-id="288a9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="288a9-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="288a9-111">Ottenere l'elenco di Vault nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="288a9-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="288a9-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="288a9-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="288a9-113">Ottenere l'elenco di Vault nel gruppo di risorse nell'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="288a9-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="288a9-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="288a9-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="288a9-115">Ottenere il Vault nel gruppo di risorse con il nome assegnato.</span><span class="sxs-lookup"><span data-stu-id="288a9-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="288a9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="288a9-116">PARAMETERS</span></span>

### <span data-ttu-id="288a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288a9-117">-DefaultProfile</span></span>

<span data-ttu-id="288a9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="288a9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="288a9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="288a9-119">-Name</span></span>

<span data-ttu-id="288a9-120">Specifica il nome del Vault a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="288a9-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="288a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288a9-121">-ResourceGroupName</span></span>

<span data-ttu-id="288a9-122">Specifica il nome del gruppo di risorse Azure da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="288a9-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="288a9-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="288a9-123">-Tag</span></span>

<span data-ttu-id="288a9-124">Specifica i tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="288a9-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="288a9-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="288a9-125">-TagName</span></span>

<span data-ttu-id="288a9-126">Specifica la chiave del tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="288a9-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="288a9-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="288a9-127">-TagValue</span></span>

<span data-ttu-id="288a9-128">Specifica il valore del tag a cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="288a9-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="288a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288a9-129">CommonParameters</span></span>
<span data-ttu-id="288a9-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288a9-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="288a9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288a9-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="288a9-132">INPUTS</span></span>

### <span data-ttu-id="288a9-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="288a9-133">None</span></span>

## <span data-ttu-id="288a9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="288a9-134">OUTPUTS</span></span>

### <span data-ttu-id="288a9-135">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="288a9-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="288a9-136">Note</span><span class="sxs-lookup"><span data-stu-id="288a9-136">NOTES</span></span>

## <span data-ttu-id="288a9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="288a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="288a9-138">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="288a9-138">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="288a9-139">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="288a9-139">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="288a9-140">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="288a9-140">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
