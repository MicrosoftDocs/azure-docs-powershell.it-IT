---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 68a9c47f3d5f5313a84729d0a7e0cdd5a2c3fac4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674701"
---
# <span data-ttu-id="86660-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="86660-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="86660-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86660-102">SYNOPSIS</span></span>
<span data-ttu-id="86660-103">Ottiene informazioni sugli account di condivisione dati</span><span class="sxs-lookup"><span data-stu-id="86660-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="86660-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86660-104">SYNTAX</span></span>

### <span data-ttu-id="86660-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86660-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86660-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="86660-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86660-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86660-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86660-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86660-108">DESCRIPTION</span></span>
<span data-ttu-id="86660-109">Il cmdlet **Get-AzDataShareAccount** ottiene le informazioni sugli account DataShare in un gruppo di risorse o abbonamenti di Azure.</span><span class="sxs-lookup"><span data-stu-id="86660-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="86660-110">Se specifichi il nome di un account, questo cmdlet ottiene le informazioni sull'account di datshare.</span><span class="sxs-lookup"><span data-stu-id="86660-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="86660-111">Se non specifichi un nome, questo cmdlet recupera le informazioni su tutti gli account di DataShare in un gruppo di risorse o abbonamenti di Azure.</span><span class="sxs-lookup"><span data-stu-id="86660-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="86660-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86660-112">EXAMPLES</span></span>

### <span data-ttu-id="86660-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86660-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="86660-114">Questo comando Visualizza le informazioni su tutti gli account di condivisione dati nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="86660-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="86660-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86660-115">PARAMETERS</span></span>

### <span data-ttu-id="86660-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86660-116">-DefaultProfile</span></span>
<span data-ttu-id="86660-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86660-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86660-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="86660-118">-Name</span></span>
<span data-ttu-id="86660-119">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="86660-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86660-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86660-120">-ResourceGroupName</span></span>
<span data-ttu-id="86660-121">Nome del gruppo di risorse dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="86660-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86660-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86660-122">-ResourceId</span></span>
<span data-ttu-id="86660-123">ID risorsa dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="86660-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86660-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86660-124">CommonParameters</span></span>
<span data-ttu-id="86660-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86660-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86660-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86660-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86660-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86660-127">INPUTS</span></span>

### <span data-ttu-id="86660-128">System. String</span><span class="sxs-lookup"><span data-stu-id="86660-128">System.String</span></span>

## <span data-ttu-id="86660-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86660-129">OUTPUTS</span></span>

### <span data-ttu-id="86660-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="86660-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="86660-131">Note</span><span class="sxs-lookup"><span data-stu-id="86660-131">NOTES</span></span>

## <span data-ttu-id="86660-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86660-132">RELATED LINKS</span></span>
