---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201076"
---
# <span data-ttu-id="f7eaf-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f7eaf-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="f7eaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="f7eaf-103">Ottiene i dettagli di un account di ANF (Azure NetApp files).</span><span class="sxs-lookup"><span data-stu-id="f7eaf-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="f7eaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7eaf-104">SYNTAX</span></span>

### <span data-ttu-id="f7eaf-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7eaf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7eaf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7eaf-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7eaf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7eaf-107">DESCRIPTION</span></span>
<span data-ttu-id="f7eaf-108">Il cmdlet **Get-AzNetAppFilesAccount** ottiene i dettagli di un account ANF.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="f7eaf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7eaf-109">EXAMPLES</span></span>

### <span data-ttu-id="f7eaf-110">Esempio 1: ottenere un account di ANF</span><span class="sxs-lookup"><span data-stu-id="f7eaf-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="f7eaf-111">Questo comando consente di ottenere l'account denominato MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="f7eaf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7eaf-112">PARAMETERS</span></span>

### <span data-ttu-id="f7eaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7eaf-113">-DefaultProfile</span></span>
<span data-ttu-id="f7eaf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7eaf-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7eaf-115">-Name</span></span>
<span data-ttu-id="f7eaf-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="f7eaf-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f7eaf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7eaf-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7eaf-118">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="f7eaf-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f7eaf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7eaf-119">-ResourceId</span></span>
<span data-ttu-id="f7eaf-120">ID risorsa dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="f7eaf-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="f7eaf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7eaf-121">CommonParameters</span></span>
<span data-ttu-id="f7eaf-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7eaf-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7eaf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7eaf-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7eaf-124">INPUTS</span></span>

### <span data-ttu-id="f7eaf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f7eaf-125">System.String</span></span>

## <span data-ttu-id="f7eaf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7eaf-126">OUTPUTS</span></span>

### <span data-ttu-id="f7eaf-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f7eaf-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f7eaf-128">Note</span><span class="sxs-lookup"><span data-stu-id="f7eaf-128">NOTES</span></span>

## <span data-ttu-id="f7eaf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7eaf-129">RELATED LINKS</span></span>
