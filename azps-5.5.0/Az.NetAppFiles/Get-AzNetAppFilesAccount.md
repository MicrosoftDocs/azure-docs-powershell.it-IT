---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187310"
---
# <span data-ttu-id="41305-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="41305-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="41305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41305-102">SYNOPSIS</span></span>
<span data-ttu-id="41305-103">Recupera i dettagli di un account Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="41305-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="41305-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41305-104">SYNTAX</span></span>

### <span data-ttu-id="41305-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41305-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41305-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41305-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41305-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41305-107">DESCRIPTION</span></span>
<span data-ttu-id="41305-108">Il cmdlet **Get-AzNetAppFilesAccount** ottiene i dettagli di un account ANF.</span><span class="sxs-lookup"><span data-stu-id="41305-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="41305-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41305-109">EXAMPLES</span></span>

### <span data-ttu-id="41305-110">Esempio 1: Ottenere un account ANF</span><span class="sxs-lookup"><span data-stu-id="41305-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="41305-111">Questo comando recupera l'account denominato AccountAnf.</span><span class="sxs-lookup"><span data-stu-id="41305-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="41305-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41305-112">PARAMETERS</span></span>

### <span data-ttu-id="41305-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41305-113">-DefaultProfile</span></span>
<span data-ttu-id="41305-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41305-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41305-115">-Name</span><span class="sxs-lookup"><span data-stu-id="41305-115">-Name</span></span>
<span data-ttu-id="41305-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="41305-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41305-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41305-117">-ResourceGroupName</span></span>
<span data-ttu-id="41305-118">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="41305-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41305-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41305-119">-ResourceId</span></span>
<span data-ttu-id="41305-120">ID risorsa dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="41305-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="41305-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41305-121">CommonParameters</span></span>
<span data-ttu-id="41305-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41305-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41305-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41305-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41305-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="41305-124">INPUTS</span></span>

### <span data-ttu-id="41305-125">System.String</span><span class="sxs-lookup"><span data-stu-id="41305-125">System.String</span></span>

## <span data-ttu-id="41305-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41305-126">OUTPUTS</span></span>

### <span data-ttu-id="41305-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="41305-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="41305-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="41305-128">NOTES</span></span>

## <span data-ttu-id="41305-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41305-129">RELATED LINKS</span></span>
