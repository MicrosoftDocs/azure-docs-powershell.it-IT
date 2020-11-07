---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: dbe206a744cc0a80d166d93b09ff0ab000cb3bc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678743"
---
# <span data-ttu-id="7cc07-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7cc07-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="7cc07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cc07-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc07-103">Ottiene i dettagli di un account di ANF (Azure NetApp files).</span><span class="sxs-lookup"><span data-stu-id="7cc07-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="7cc07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cc07-104">SYNTAX</span></span>

### <span data-ttu-id="7cc07-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7cc07-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc07-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc07-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cc07-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cc07-107">DESCRIPTION</span></span>
<span data-ttu-id="7cc07-108">Il cmdlet **Get-AzNetAppFilesAccount** ottiene i dettagli di un account ANF.</span><span class="sxs-lookup"><span data-stu-id="7cc07-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="7cc07-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cc07-109">EXAMPLES</span></span>

### <span data-ttu-id="7cc07-110">Esempio 1: ottenere un account di ANF</span><span class="sxs-lookup"><span data-stu-id="7cc07-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="7cc07-111">Questo comando consente di ottenere l'account denominato MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="7cc07-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="7cc07-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cc07-112">PARAMETERS</span></span>

### <span data-ttu-id="7cc07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc07-113">-DefaultProfile</span></span>
<span data-ttu-id="7cc07-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cc07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc07-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cc07-115">-Name</span></span>
<span data-ttu-id="7cc07-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="7cc07-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc07-117">-ResourceGroupName</span></span>
<span data-ttu-id="7cc07-118">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="7cc07-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc07-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cc07-119">-ResourceId</span></span>
<span data-ttu-id="7cc07-120">ID risorsa dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="7cc07-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc07-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc07-121">CommonParameters</span></span>
<span data-ttu-id="7cc07-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc07-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7cc07-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc07-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc07-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cc07-124">INPUTS</span></span>

### <span data-ttu-id="7cc07-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc07-125">System.String</span></span>

## <span data-ttu-id="7cc07-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cc07-126">OUTPUTS</span></span>

### <span data-ttu-id="7cc07-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7cc07-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7cc07-128">Note</span><span class="sxs-lookup"><span data-stu-id="7cc07-128">NOTES</span></span>

## <span data-ttu-id="7cc07-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cc07-129">RELATED LINKS</span></span>
